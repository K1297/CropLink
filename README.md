  <div align="center">
  <h1>CropLink</h1>
  <p>
    <strong>An AgriTech Dapp with weather-savvy smart contracts for bountiful selling</strong>
  </p>
  
</div>                                           
                            
          
CropLink is a decentralized application (DApp) built on the Ethereum blockchain that facilitates the interaction between farmers and buyers in the agricultural produce market. It allows farmers to register, add their produce for sale, and claim treasury benefits. Buyers can register, purchase produce, and support the local farming community.

# Features

* Farmer Registration: Farmers can register themselves in the DApp by calling the registerAsFarmer() function.

* Buyer Registration: Buyers can register themselves in the DApp by calling the registerAsBuyer() function.

* Farmer Verification: Farmers have the option to verify their identity by uploading their government ID through the verifyFarmer() function.

* Buyer Verification: Buyers are required to verify their identity by uploading their government ID through the verifyBuyer() function.

* Treasury Benefits: Verified farmers can claim treasury benefits every month by calling the claimTreasury() function. Each verified farmer can claim up to 0.05 ETH per month from the treasury's total holding, which is initially set to 5 ETH.

* Produce Management: Farmers can add their produce to the sale list by providing the name, quantity, and price of the produce through the addProduce() function.

* Transferring Funds: Buyers can purchase produce from the sale list by calling the purchaseProduce() function and providing the correct amount of funds. The funds are then transferred from the buyer to the farmer's address through the transferFunds() function.

* Chainlink Integration: The DApp integrates with Chainlink to fetch data feeds such as demand, supply, weather information, and truflation data. This integration enhances the functionality and accuracy of the DApp.

* Selling Produce at Market Price: The DApp checks the weather conditions through the checkWeather() function and triggers the selling of produce at market price if heavy rain is detected. The sellProduceAtMarketPrice() function handles the logic for selling the produce at market price and transferring funds to the farmer's address.

# Chainlink Integration

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
