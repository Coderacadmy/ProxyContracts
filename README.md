# ProxyContracts Deployment commands

-------------- Proxy Contracs commands --------------
    
    
    Proxy Commands
    
    npm init -y
    npm install --save-dev hardhat
    npx hardhat 
    npm install --save-dev @openzeppelin/hardhat-upgrades
    npm install --save-dev @nomiclabs/hardhat-ethers ethers
    npm install --save-dev chai
    npm install @openzeppelin/contracts-upgradeable
    
    
    npx hardhat run scripts/deploy.js
    npx hardhat console --network ropsten
    const Box = await ethers.getContractFactory("Box")
    const box = await Box.attach("0xc64d3362E8C3273d0C263c79a5687F6998380c50")
    (await box.retrieve()).toString()
    
    
    npx hardhat run scripts/upgrade.js
    
    npx hardhat console
    const BoxV2 = await ethers.getContractFactory("BoxV2")
    const boxV2 = await BoxV2.attach("0xc64d3362E8C3273d0C263c79a5687F6998380c50")
    (await boxV2.retrieve()).toString()
    await boxV2.increment()
    (await boxV2.retrieve()).toString()
