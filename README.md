  <div align="center">
  <h1>CropLink</h1>
  <p>
    <strong>An AgriTech Dapp with weather-savvy smart contracts for bountiful selling</strong>
  </p>
  
</div>                                           
                            
          
CropLink is an AgriTech Dapp that revolutionizes the way farmers sell their produce. It provides a decentralized platform where farmers can connect with registered Sellers. Our platform leverages the power of smart contracts and Chainlink oracles to ensure fair and transparent transactions while mitigating the risks associated with unpredictable weather conditions. With the help of Chainlink oracles, CropLink constantly monitors weather patterns, including heavy rainfall that could potentially damage the farmers' produce. In such cases, smart contracts written in solidity automatically activate, enabling farmers to sell their crops to registered Sellers at their desired prices. 

By incorporating reliable data feeds, Chainlink VRF, Chainlink Keepers, and Chainlink API, CropLink ensures that farmers have access to accurate and real-time information about the prices, demand, and supply of the crops they grow, in a decentralized and secure manner. CropLink simplifies the onboarding process for farmers, who only need a Metamask account to get started. They also have the option to upload their government-authorized ID to verify their identity, unlocking additional benefits such as discounts on raw materials from our treasury fund. On the other hand, Sellers are required to register themselves using official documents authorized by the government, ensuring transparency and authenticity throughout the platform. 

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

## Chainlink Integration

The DApp integrates with Chainlink to fetch various data feeds and enhance its functionality. The following Chainlink oracles and data feeds are used:

* Demand Data: The updateProduceDemand() function triggers a Chainlink oracle to fetch produce demand data. The fulfillProduceDemand() function serves as the callback function for the demand data.

* Supply Data: The updateProduceSupply() function triggers a Chainlink oracle to fetch produce supply data. The fulfillProduceSupply() function serves as the callback function for the supply data.

* Weather Data: The checkWeather() function triggers a Chainlink oracle to fetch weather data. The fulfillWeather() function serves as the callback function for the weather data. If heavy rain is detected, it calls the sellProduceAtMarketPrice() function.

* Truflation Data: The updateTruflationData() function triggers a Chainlink oracle to fetch Truflation data. The fulfillTruflationData() function serves as the callback function for the Truflation data.


# Installation

To deploy and interact with the CropLink DApp, follow these steps:

Install the required dependencies by running npm install.

Deploy the CropLink smart contract to an Ethereum network of your choice using a development tool like Truffle or Remix.

Configure the Chainlink oracles, jobs, and data sources according to your requirements and obtain the necessary API keys.

Update the contract addresses and API keys in the DApp code.

Build and run the frontend application by running npm start.

Access the CropLink DApp through your web browser and connect it to your Ethereum wallet.

# Development

To contribute to the CropLink DApp or modify its functionality, follow these steps:

Clone the repository and navigate to the project directory.

Install the required dependencies by running npm install.

Make the necessary changes to the smart contract and DApp code.

Test the smart contract by running the provided tests with truffle test.

Build and run the frontend application by running npm start.

Verify that the modifications and new features are working as intended.

Submit a pull request detailing the changes you made.

# Troubleshooting

If you encounter any issues or errors while using the CropLink DApp, please follow these steps to troubleshoot:

Check that you have the latest version of Node.js and npm installed.

Ensure that your Ethereum wallet is properly configured and connected to the correct network.

Double-check the contract addresses and API keys in the DApp code for accuracy.

Review the error messages or console logs for any relevant information.

Consult the documentation or seek support from the CropLink team for further assistance.

# Contribution Guidelines

Thank you for considering contributing to the CropLink DApp! To contribute, please follow these guidelines:

Fork the repository and create a new branch for your contribution.

Make your changes and ensure that the code follows the project's coding standards.

Write clear and concise commit messages explaining the purpose of your changes.

Test your changes thoroughly to ensure they do not introduce any regressions.

Submit a pull request, providing a detailed description of your changes and their purpose.

Be responsive to any feedback or review comments during the review process.

# Team members 

• Cláudio Barreira 
• Kushal sapra
• Ahmidenwer
• Suleman Ismaila

# Acknowledgements

We would like to acknowledge the following individuals and resources for their contributions and support:

Chainlink for providing the infrastructure and tools for fetching data feeds and integrating them into the CropLink DApp.

The Ethereum development community for their continuous efforts in advancing decentralized applications and smart contract technology.
