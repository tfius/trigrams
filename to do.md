### option 1
 * add a contractURI method to your ERC721 or ERC1155 contract that returns a URL for the storefront-level metadata for your contract.
 
 function contractURI() public view returns (string memory) {
        return "https://metadata-url.com/my-metadata";
 }
 
 return URL example:
 {
  "name": "Type name",
  "description": "OpenSea Creatures are adorable aquatic beings primarily for demonstrating what can be done using the OpenSea platform. Adopt one today to try out all the OpenSea buying, selling, and bidding feature set.",
  "image": "https://openseacreatures.io/image.png",
  "external_link": "https://openseacreatures.io",
  "seller_fee_basis_points": 100, # Indicates a 1% seller fee.
  "fee_recipient": "0xA97F337c39cccE66adfeCB2BF99C1DdC54C2D721" # Where seller fees will be paid to.
}

### metadata
{
  "description": "Friendly OpenSea Creature that enjoys long swims in the ocean.", 
  "external_url": "https://openseacreatures.io/3", 
  "image": "https://storage.googleapis.com/opensea-prod.appspot.com/puffs/3.png", 
  "name": "Dave Starbelly",
  "attributes": [ ... ], 
}


### Freezing Metadata
You can indicate to OpenSea that an NFT's metadata is no longer changeable by anyone (in other words, it is "frozen") by emitting this event from the smart contract:

event PermanentURI(string _value, uint256 indexed _id);

### option 2
https://docs.opensea.io/docs/opensea-integration

{
  "description": "Friendly OpenSea Creature that enjoys long swims in the ocean.", 
  "external_url": "https://openseacreatures.io/3", 
  "image": "https://storage.googleapis.com/opensea-prod.appspot.com/puffs/3.png", 
  "name": "Dave Starbelly",
  "attributes": [ ... ], 
}
 
