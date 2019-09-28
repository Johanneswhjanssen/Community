# people

People of liquid communities represent real, physical people of flesh and blood with one and only one voice. It is not permitted for a person to be a member of a social identity several times and thus to have the right to vote multiple times. A person is of course not allowed to register under the name of another person (identity fraud). The identification of persons is a difficult problem in the world of the internet and the blockchain. Anyone can create 10 accounts in an online store, with 10 different email addresses, and buy something under each account. The internet store does not care. It just wants to sell. The blockchain is also not interested in the identity or identification of people, but only in transactions. A person can have multiple accounts, tokens, wallets, bank accounts (such as a bitcoin account or the ethereal account) in the blockchain. There is no (world) standard for identifying people yet. Many initiatives are being undertaken to develop such a standard, such as SSI (self-sovereign identity) or the ERC725 proposal by Fabian Vogelsteller.  (https://www.youtube.com/watch?v=qF2lhJzngto, https://www.youtube.com/watch?v=jjUKWRK8H2g). All initiatives have different perspectives. A good identity registration should combine a physical body characteristic (thumbprint, iris, DNA etc.) with a mental characteristic (a personal code given by the system and a personal password) and an active verification (such as 2 fold Authentication).
The People contract currently opts for a traditional solution: we have the identification performed by one or more identity managers. Each method of identification is assessed with a weight (a number). The higher the weight, the more certain the identification. Above a certain value, the status of the person changes to adult. At that time the person can participate in communities and start communities themselves. Only an adult person is entitled to vote.
Identity managers should perform the identification as a neutral process and should be mixed with political choices or preferences. It is up to the community / administration to draw up rules for political boundaries.

In the human contract the person receives a unique personal number. It is connected to one or more accounts/adresses. If the person is a member of a social identity, one of his accounts will be the 'identifier' of that person within the social identity. A person can enter an alias as a name within each social identity.

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

    function identityMove(address peopleTarget, address connectionAdministrator) public returns (bool success) {}
    function communityMove(address identitySource, address identityTarget, address communityToMove) public returns (bool success) {}

      An identity can decide to be moved to another People contract. A community can decide to become (part of) another social identity. This function is not a Relations function, because its concerns movement on a higer level. Relations concern interactions between communities of one social identity.

    function isIdentity (address identityContract)  public view returns (bool){}
    function isPerson (address checkPerson) public view returns (uint){}
    function isPersonConnected (address personAddress) public returns (address,uint){}
    function isPersonByCode (string personCode, address checkPerson) public view returns (uint){}
    function isIdentityAdministrator (address checkPerson) public view returns (uint){}
    function getPersonStateName (uint8 st) public pure returns (string memory){}
    function getPersonCategoryName (uint8 cat) public pure returns (string memory){}

      Functions returning a boolean: checking some property.
}
