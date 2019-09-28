# people

Mensen van een vloeibare gemeenschappen representeren echte, fysieke mensen van vlees en bloed met een en slechts een stem. Het is niet toegestaaan dat een persoon meerdere keren lid is binnen een sociale identiteit en daarmee het recht zou verkrijgen  meerdere keren te stemmen. Een persoon mag zich ook niet onder de naam van een andere persoon registreren (identiteitsfraude). De identificatie van personen is in wereld van het internet en de blockchain een lastig probleem. Iedereen kan in een internetwinkel 10 accounts aanmaken, met 10 verschillende emailadressen, en onder elk account iets kopen. De internet-winkel zit daar niet mee. Het wil alleen maar verkopen. Ook de blockchain is niet geintereseerd in de identiteit of de identificatie van mensen, maar alleen in transacties. Een persoon kan in de blockchain meerdere  accounts, tokens, portomonees, bankrekeningen (zoals een bitcoin-rekening of de ethereum rekening) hebben. Er bestaat nog geen (wereld)standaard voor het identificateren van mensen. Veel initiatieven worden ontplooid om zo'n standaard te ontwikkelen, zoals SSI (self sovereign identity) of het ERC725 voorstel van Fabian Vogelsteller (https://www.youtube.com/watch?v=qF2lhJzngto, https://www.youtube.com/watch?v=jjUKWRK8H2g). Alle initiatieven hebben verschillende invalshoeken. Een goede identiteitsregistratie zou een fysiek lichaamskenmerk (duimafdruk, iris, DNA etc.) moeten combineren met een geestelijke  kenmerk (een persoonscode gegeven door het systeem en een eigen wachtwoord) en een actieve verificatie (zoals 2 fold Authentication).
Het People contract kiest voorlopig voor een klassieke oplossing: we laten de identificatie uitvoeren door een of meerdere identiteitsbeheerders. Elke methode van identitificatie wordt beoordeeld met een gewicht (een getal). Hoe hoger het gewicht, hoe zekerder de identificatie. Boven een bepaalde waarde wijzigt de status van de persoon naar volwassen. Op dat moment kan de persoon deelnemen aan gemeenschappen en zelf gemeenschappen starten.  Alleen een volwassen persoon is stemgerechtigd.
Identiteitsbeheerders dienen de identificatie uit te voeren als een neutraal proces en mag niet vermengd zijn moet politieke keuzes of voorkeuren. Het is aan de gemeenschap/bestuur hier regels voor op te stellen.

## contract functions

contract People {
    constructor (string adminCode, string adminName) public {}
    function peopleAdminChange(string newAdminCode, address checkAccount, bool transferMyRights) public {}

    The creator of a people contract will be its first person, and the first people administrator. The main task of the people administrator is to identify persons. The first person itself can not be identified. The administrator can not be deleted, but he or she can transfer its function to an other (identified) person. When the people contract increases in number of persons extra people Administrators have to be added.
    A people administrator can of course join multiple social identities. But the rule of contract is he or can can only be servant of (the communities of) that social identity.  

    function personAdd(string newPersonCode, string newName, address newAccount) public {}
    function personAddIdentity(uint id, address identityAddress) public returns (uint){}
    function PersonGenerateCode() internal returns (string[6]) {}
    function personDelete(string personCode, string personName, address deleteAccount, uint methodOfVerification) public {}
    function personSetState (uint id, uint changeToState) public returns (uint currentState) {}
    function personInfo (address personAddress)  public view returns (string, string, string, uint) {}
    function personUpdate(string personCode, string personName, uint newCategory, uint methodOfVerification) public returns (string, string, string) {}

    These functions are used to update the person entitiy (struct).  

    function identityAdd(address newIdentityContract) public returns (bool succes) {}
    function identityDelete(address deletedIdentity) public returns (bool succes) {}
    function identityList() public view returns (address[]) {}

    The people contract stores a list of all social identities persons can join after they have been identified. The social identity is added by the constructor function of the social identiy itself.

    function peopleConnect(address newConnection, address connectionAdministrator) public returns (bool success) {}
    function communityMove(address identitySource, address identityTarget, address communityToMove) public returns (bool success) {}

    function isIdentity (address identityContract)  public view returns (bool){}
    function isPerson (address checkPerson) public view returns (uint){}
    function isPersonConnected (address personAddress) public returns (address,uint){}
    function isPersonByCode (string personCode, address checkPerson) public view returns (uint){}
    function isIdentityAdministrator (address checkPerson) public view returns (uint){}
    function getPersonStateName (uint8 st) public pure returns (string memory){}
    function getPersonCategoryName (uint8 cat) public pure returns (string memory){}
}
