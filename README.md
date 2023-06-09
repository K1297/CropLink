  <div align="center">
  <h1>CropLink</h1>
  <p>
    <strong>An AgriTech Dapp with weather-savvy smart contracts for bountiful selling</strong>
  </p>
  
</div>                                           
                            
          
CropLink is an AgriTech Dapp that revolutionizes the way farmers sell their produce. It provides a decentralized platform where farmers can connect with registered Sellers. Farmers can list & add their produce, including name, quantity, and price for sale. They can view and manage their list of produce. Our platform leverages the power of smart contracts and Chainlink oracles to ensure fair and transparent transactions while mitigating the risks associated with unpredictable weather conditions. With the help of Chainlink oracles, CropLink constantly monitors weather patterns, including heavy rainfall that could potentially damage the farmers' produce. In such cases, smart contracts written in solidity automatically activate, enabling farmers to sell their crops to registered Sellers.

CropLink simplifies the onboarding process for farmers, who only need a Metamask account to get started. They also have the option to upload their government-authorized ID to verify their identity, unlocking additional benefit of montly claim from our treasury fund.

Additionally, CropLink utilizes AWS services to enhance the scalability and reliability of our platform, providing a seamless experience for all users.

# CropLink code Repositories

# Features

* **Registration**: Farmers and buyers can register themselves on the platform.
* **Verification**: Farmers and buyers can verify their identities to access additional features like claim from our treasury.
* **Add Produce**: Farmers can add their produce, including name, quantity, and price.
* **Produce Listing**: Farmers can view and manage their list of produce.
* **Update Produce**: Farmers can update the quantity of produce based on real-time demand and supply data.
* **Weather Check**: Buyers can check weather conditions through Chainlink oracles.
* **Purchase Produce**: Buyers can purchase produce securely.
* **Treasury Fund**: Verified farmers can claim benefits from the treasury fund.

# Architecture

## Components

* **Frontend**: This is the user interface where farmers and sellers interact with the Dapp. It can be a
web-based interface.
* **Sign in with metamask**: Users can connect their accounts using a MetaMask.
* **Backend**: This is the server-side of the Dapp. 
* **AWS**: AWS provides for storing user data, and networking for communication between different components.
* **Dynamo DB**: Dynamo DB for storing user data.
* **CropLink smart contract**: The smart contracts written in Solidity. It includes the core logic of the Dapp, including functions for farmers to sell their produce, sellers to buy produce. 
* **Chainlink**: The Chainlink is responsible for fetching external data, such as weather
information.
* **Accuweather**: Accuweather used for fetching weather confitions.


# Local Installation

1. Clone the repository

First, you need to clone the repository
```
git clone https://github.com/claudioBarreira89/croplink.git
```

2. Install Dependencies

Install the project's dependencies using Yarn:

```
yarn install
```

3. Start the Project

Once all the dependencies are installed, you can start the project:

```
yarn dev
```

The project should now be running on `http://localhost:3000`

# Environment Variables

This project uses environment variables for configuration. These variables should be stored in a `.env` file in the root directory of the project.

Here is an example of what your `.env` file should look like:

```
PORT=3000
IRON_SESSION_PW=YOUR_VARIABLE
AWS_ACCESS_KEY_ID=YOUR_VARIABLE
AWS_SECRET_ACCESS_KEY=YOUR_VARIABLE
AWS_DEFAULT_REGION=YOUR_VARIABLE
```

# Usage

* Farmers and Buyers can register on the CropLink DApp to participate in the platform by connecting metamask.
* Registered farmers can verify their identity by uploading their government ID to get verified.
* Verified farmers can claim monthly treasury benefits.
* Farmers can list their produce for sale on the CropLink DApp.
* Buyers can browse and purchase available produce listings.
* Users can sell their produce in case of heavy rain and receive on current weather conditions.

# Smart Contract Documentation

## Contract Structure
The CropLink smart contract is implemented in Solidity and consists of the following main components:

### Structs:

* **Produce**: Represents an agricultural product with properties such as name, quantity, price, sold status, index, and farmer address.
* **MarketPrice**: Holds the buyer's address and the price they are willing to pay for produce.
* **WeatherData**: Contains weather condition information and a flag indicating if it's rainy.

### Variables:

* **private constant ORACLE_PAYMENT**: Represents the payment required to use Chainlink oracles.
* **treasury**: Address of the treasury account where funds are deposited.
* **treasuryBalance**: Current balance in the treasury.
* **temperature**: Holds the temperature retrieved from the weather oracle.
* **link**: Instance of the Chainlink LinkTokenInterface for interacting with the LINK token.
* **farmerAddresses**: Array of registered farmer addresses.
* **buyerAddresses**: Array of registered buyer addresses.
* **farmers**: Mapping to track registered farmers.
* **buyers**: Mapping to track registered buyers.
* **farmerVerifications**: Mapping to track verified farmers.
* **produceList**: Mapping to store produce lists for each farmer.
* **marketPrices**: Mapping to store market prices set by buyers.
* **marketPriceVerified**: Mapping to track if a buyer's market price is verified.
* **requestIdToAddress**: Mapping to link Chainlink request IDs with addresses.
* **requestIdToIndex**: Mapping to link Chainlink request IDs with produce indexes.
* **requestIdToWeatherData**: Mapping to store weather data for Chainlink request IDs.

### Constructor:

Initializes the Chainlink token, sets the treasury address, and assigns an initial balance to the treasury.
Public Functions:

* **registerAsFarmer()**: Allows an address to register as a farmer.
* **registerAsBuyer()**: Allows an address to register as a buyer.
* **verifyFarmer()**: Verifies the caller as a registered farmer.
* **claimTreasury()**: Allows verified farmers to claim treasury benefits.
* **addProduce(string _name, uint256 _quantity, uint256 _price)**: Adds produce to the list for the calling farmer.
* **adjustPriceByWeather()**: Returns an adjustment value based on the temperature.
* **getFarmers()**: Returns an array of registered farmer addresses.
* **getBuyers()**: Returns an array of registered buyer addresses.
* **getAllProduceList()**: Returns an array of all produce across all farmers, along with the price adjustment based on weather.
* **getProduceList(address _farmer)**: Returns an array of produce for the specified farmer,.

# Troubleshooting

**Metamask Login Issue**

If you are unable to sign in with Metamask, please ensure that your Metamask wallet is properly configured and has sufficient funds to pay for the transaction fees. Additionally, ensure that you are signed into Metamask and have granted permission for the dapp to access your wallet.

# Contribution Guidelines
We welcome contributions from anyone who would like to help improve our decentralized content sharing dapp.

To contribute, please follow the following steps:

1. Fork the repository to your own GitHub account:
2. Create a new branch from the main branch for your changes.
3. Make your changes and commit them with clear commit messages.
4. Push your changes to your forked repository.
5. Open a pull request to merge your changes into the main branch.

# Team Members
* Cláudio Barreira
* Kushal Sapra
* Ahmed Anwer
* Suleman Ismaila
* Anna Kazannik

# Acknowledgements

We would like to acknowledge the following individuals and resources for their contributions and support:

* Chainlink for providing the infrastructure and tools for fetching weather information and integrating them into the CropLink DApp.

* The Ethereum development community for their continuous efforts in advancing decentralized applications and smart contract technology.
