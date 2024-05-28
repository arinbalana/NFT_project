// 1: Array to store NFT's
const myNFT = [];

// 2: By this function we pass different NFT's using making object inside the function
function mintNFT(name, age, sex, patentID){
  const listPatent = {
    "name" : name,
    "age" : age,
    "sex" : sex,
    "patentID" : patentID
  };
  myNFT.push(listPatent);
}

// 3: this function to print all the NFT to the console
function listNFTs(){
  for(let i = 0; i < myNFT.length; i++){
    console.log("Name: " + myNFT[i].name);
    console.log("Age: " + myNFT[i].age);
    console.log("Sex: " + myNFT[i].sex);
    console.log("Patent ID: " + myNFT[i].patentID);
    console.log("=================");   // used for seperation between different NFTs
  }
}

// 4: this function returns the number of NFTs we created
function getTotalSupply(){
  return myNFT.length;
}


// ****** function calling section ******

// minting some NFTs
mintNFT("Arin Balana", 21, "Male", 33892);
mintNFT("Ishaan", 18, "Male", 97392);
mintNFT("Neha", 20, "Female", 72892);
mintNFT("Pankaj", 15, "Male", 45672);

// listing all NFTs
listNFTs();

// printion number of NFTs
console.log("Total Supply: " + getTotalSupply());
