  <div align="center">
  <h1>CropLink</h1>
  <p>
    <strong>An AgriTech Dapp with weather-savvy smart contracts for bountiful selling</strong>
  </p>
  
</div>                                           
                            
          
CropLink is an AgriTech Dapp that revolutionizes the way farmers sell their produce. It provides a decentralized platform where farmers can connect with registered Sellers. Farmers can list & add their produce, including name, quantity, and price. They can view and manage their list of produce. Our platform leverages the power of smart contracts and Chainlink oracles to ensure fair and transparent transactions while mitigating the risks associated with unpredictable weather conditions. With the help of Chainlink oracles, CropLink constantly monitors weather patterns, including heavy rainfall that could potentially damage the farmers' produce. In such cases, smart contracts written in solidity automatically activate, enabling farmers to sell their crops to registered Sellers at their desired prices. 

By incorporating reliable data feeds, Chainlink VRF, Chainlink Keepers, and Chainlink API, CropLink ensures that farmers have access to accurate and real-time information about the prices, demand, and supply of the crops they grow, in a decentralized and secure manner. CropLink simplifies the onboarding process for farmers, who only need a Metamask account to get started. They also have the option to upload their government-authorized ID to verify their identity, unlocking additional benefit of montly claim from our treasury fund. On the other hand, Sellers are required to register themselves using official documents authorized by the government, ensuring transparency and authenticity throughout the platform. 

Additionally, CropLink utilizes AWS services to enhance the scalability and reliability of our platform, providing a seamless experience for all users.

# CropLink code Repositories

# Features

* **Registration**: Farmers and buyers can register themselves on the platform.
* **Verification**: Farmers and buyers can verify their identities to access additional features.
* **Add Produce**: Farmers can add their produce, including name, quantity, and price.
* **Produce Listing**: Farmers can view and manage their list of produce.
* **Update Demand**: Farmers can update the quantity of produce based on real-time demand data retrieved from Chainlink oracles.
* **Update Supply**: Farmers can update the quantity of produce based on real-time supply data retrieved from Chainlink oracles.
* **Weather Check**: Buyers can check weather conditions through Chainlink oracles.
* **Purchase Produce**: Verified buyers can purchase produce securely.
* **Treasury Fund**: Verified farmers can claim benefits from the treasury fund.

# Architecture

## Components

* **Frontend**: This is the user interface where farmers and sellers interact with the Dapp. It can be a
web-based interface accessible through a browser, and users can connect their accounts using a
tool like MetaMask.
* **Backend**: The backend consists of smart contracts written in Solidity. It
includes the core logic of the Dapp, including functions for farmers to sell their produce, sellers to
buy produce, and retrieving price, demand, and supply information from the Chainlink Oracle.
* **Chainlink Oracle**: The Chainlink Oracle is responsible for fetching external data, such as weather
information and market prices, and providing it to the smart contracts. It can use Chainlink
Keepers, Data Feeds, or APIs to retrieve and update data. In this case, the oracle checks weather
conditions, such as heavy rainfall, which may affect the produce.
* **Truflation Data**: Truflation Data is an external service that provides accurate and reliable market
data related to produce prices, demand, and supply. The Chainlink Oracle can use this service to
retrieve the required information and feed it into the smart contracts.
* **AWS Services**: AWS provides a range of cloud services that can be utilized by the Dapp. This
includes storage for storing user data, compute for running backend processes, and networking
for communication between different components.

# Local Installation

# Usage

* Farmers can register on the CropLink DApp to participate in the platform by connecting metamask.
* Buyers can register on the CropLink DApp to access and purchase produce by connecting metamask.
* Registered farmers can verify their identity by uploading their government ID.
* Farmers can list their produce for sale on the CropLink DApp.
* Buyers can browse and purchase available produce listings.
* Users can check and receive updates on current weather conditions.
* Verified farmers can claim monthly treasury benefits.
* Users can update the demand and supply data for specific produce using Chainlink APIs.
* Users can update Truflation data using a Chainlink API.

# Smart Contract Documentation

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

* Chainlink for providing the infrastructure and tools for fetching data feeds and integrating them into the CropLink DApp.

* The Ethereum development community for their continuous efforts in advancing decentralized applications and smart contract technology.
