# identificatie

Mensen van (vloeibare) gemeenschappen representeren echte, fysieke mensen van vlees en bloed met een en slechts een stem. Het is niet toegestaaan dat een persoon meerdere keren lid is binnen een sociale identiteit en daarmee het recht zou verkrijgen  meerdere keren te stemmen. Een persoon mag zich ook niet onder de naam van een andere persoon registreren (identiteitsfraude). De identificatie van personen is in wereld van het internet en de blockchain een lastig probleem. Iedereen kan in een internetwinkel 10 accounts aanmaken, met 10 verschillende emailadressen, en onder elk account iets kopen. De internet-winkel zit daar niet mee. Het wil alleen maar verkopen. Ook de blockchain is niet geintereseerd in de identiteit of de identificatie van mensen, maar alleen in transacties. Een persoon kan in de blockchain meerdere  accounts, tokens, portomonees, bankrekeningen (zoals een bitcoin-rekening of de ethereum rekening) hebben. Er bestaat nog geen (wereld)standaard voor het identificateren van mensen.

Veel initiatieven worden ontplooid om zo'n standaard te ontwikkelen, zoals SSI (self sovereign identity) of het ERC725 voorstel van Fabian Vogelsteller (https://www.youtube.com/watch?v=qF2lhJzngto, https://www.youtube.com/watch?v=jjUKWRK8H2g). Alle initiatieven hebben verschillende invalshoeken. Een goede identiteitsregistratie zou een fysiek lichaamskenmerk (duimafdruk, iris, DNA etc.) moeten combineren met een geestelijke  kenmerk (een persoonsID  en een wachtwoord) en een actieve verificatie via bijvoorbeeld een SMS moeten hebben. Maar dat ook dat veel persoonskenmerken in de blockchain moeten worden geregisteerd. Identificatie is in essentie alleen mogelijk door een centrale registratie vast te leggen. Dat staat haaks op de decentrale uitgangspunten van de blockchain. Beide zijn niet te verenigen tenzij de blockchain gevuld wordt met grote hoeveelheden privegegevens, maar dan wordt de privacy van gebruikers te sterk aangetast.

Het identificatie-contract van deze Dapp kiest kiest (voorlopig!) voor de klassieke oplossing: we laten de identificatie uitvoeren door een of meerdere beheerders. De beheerders dienen te registreren welke methode van identificatie is gebruikt. Elke methode van identitificatie wordt beoordeeld met een gewicht (een getal). Hoe hoger het gewicht, hoe zekerder de identificatie. Een persoon kan deelnemen aan gemeenschappen als de zekerheid van identificatie een bepaalde waarde overstijgt. De persoonscategorie wijzigt van 'Onderzoek' naar 'Persoon'. Indien iemand van de gemeenschap twijfelt aan de identiteit van een persoon kan hij of zij een 'challenge' aanvragen bij identiteitsmanangers. Een andere identiteitsmanager verifieert (of falsifieert) de eerdere identificatie.

Iedereen ontvangt een ID in het identificatiecontract. Dit ID is vergelijkbaar met bijv. een Paspoort-nummer. Er is bewust voor gekozen om geen ID-kenmerken uit de reele wereld in de blockchain op te nemen, omdat deze allemaal beperkingen hebben. Er zijn heel veel verschillende systemen, die identificatie-conflicten veroorzaken. Paspoorten kunnen worden gestolen, statenlozen hebben geen paspoorten. Er kunnen fictieve paspoorten/identiteiten worden gemaakt. Het ID is niet gerelateerd aan een fysiek address. Het is een blockchain ID die, overal in de wereld en buiten de wereld gelijk is.

Identificatiecontracten zijn in principe zelfstandige basisregistraties die onafhankelijk van elkaar bestaan. Iedereen kan zelf een identificatiecontract starten, om vervolgens daarbinnnen een gemeenschap te starten. Een oprichter van een gemeenschap kan echter ook binnen een reeds bestaande identificatiecontract zijn gemeenschap starten. Dit zal afhangen van de bekendheid, de betrouwbaarheid van het identificatie-contract en van de mogelijk beoogde samenwerkingen met andere gemeenschappen (relatie contract). De Dapp heeft een functie die heet 'CommunityMove'. Een gemeenschap kan besluiten naar een ander Mens contract te verhuizen binen dezelfde identificatiecontract (geen persoonswijzigingen) Een Mens contract kan ook verhuizen naar een ander identificatiecontract. In dat geval dienen de idenficatiecontracten met elkaar te worden verbonden, waarbij gelijktijdig alle personen van de bron-gemeenschap de persoonsstatus 'checking' krijgen. De identiteitsmanagers van de doel-conctract, moeten iedereen van de bron contract identificeren en alle dubbelingen er uit halen. Het doel van de CommunityMove function is om gemeenschappen die het vertrouwen in de identificatiemanagers van een contract verloren hebben een uitweg te bieden, waardoor de gemeenschappen behouden blijft. Maar ook om uiteindelijk slechts 1 wereldwijd netwerk van identificaitecontracten  over te houden waarin ieder mens altijd een unieke ID heeft.

uitzoeken: people contract overzetten, dan alle mensen opnieuw laten inschrijven bij nieuwe identificatiecontract?
of toch koppelen, maar dan blijft oude identificatie in beeld (personen staan daar)

Identiteitsbeheerders dienen de identificatie uit te voeren als een neutraal proces en mag niet vermengd zijn moet politieke keuzes of voorkeuren. Het is aan de gemeenschap/bestuur hier regels voor op te stellen.

## structure

struct Person {                        // the person represents a unique human being
        string name;                   // The name of the person
        uint8 cat;                     // categoy of the person
        uint8 state;                   // state of the person
        uint8 methodOfId1;             // method number used to identify you as a person
        address idBy1;                 // address of idenititymananger which changed methodOfId1
        uint8 methodOfId2;             // method number used to identify you as a person (challenged ID)
        address idBy2;                 // address of idenititymananger which changed methodOfId2
        uint changed;                  // time last change
        address changedBy;             // address of person who performed last change
        address[] peopleContracts;      // the  people contracts this person is member of
    }

## definitie van statussen en categorieen

    function getPersonStateName (uint8 st) public pure returns (string memory){
      if (st==0) return "";
      if (st==100) return "Checking";   // is used to (Re-)identify a person
      if (st==200) return "Challenging";  // is used to identify person by second IdAdministrator
      if (st==300) return "Identified"; // identified person who can now become member of communities
      if (st==400) return "Deleted";   // an identified person who has died or has quit, equal to first state
                                     // but there is some history in the blockchain
      }

      function getPersonCategoryName (uint8 cat) public pure returns (string memory){
      if (cat==0) return "";            // no yet known, initial category
      if (cat==100) return "Child";     // an identified person who has not yet a legal age to vote in a community
      if (cat==200) return "Person";    // an identified person who can vote

      function getMethodOfIdentification (uint8 method) public pure returns (string memory){
      if (method==0) return "";
      if (method==100) return "identified by social media";
      if (method==500) return "identified by official governmental sites";
      if (method==600) return "identified identificationAdminstrator";
      if (method==980) return "identified by other persons: claim-holders greater 500";
      if (method==999) return "Creator of this Identification-contract, no identification";

## notes on contract functions

contract Identification {
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
