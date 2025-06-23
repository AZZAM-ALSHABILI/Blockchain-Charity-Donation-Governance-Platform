Blockchain Charity Donation & Governance Platform
This project is a fully functional decentralized application (DApp) that provides a transparent, secure, and decentralized way to manage and track donations using blockchain technology. It features a robust, role-based system for public donors, registered NGOs, and a platform administrator, complete with a community-driven governance model for key decisions.

The platform is split into three main user-facing components:
Home Page (home.html): A public landing page introducing the platform's mission and features.
Public Portal (public.html): The main portal for donors and NGOs to interact with the platform's features.
Admin Dashboard (admin.html): A restricted-access dashboard for the platform owner to manage core contract functionalities.

Core Concepts
Role-Based Access: The DApp enforces a clear distinction between three user types: the Admin (contract owner), registered NGOs, and public Donors. Each role has a specific set of permissions and capabilities defined within the smart contract.
Decentralized Governance: Donors collectively participate in the platform's governance. Once a user makes a donation, they are granted voting rights  on proposals, such as registering new NGOs or updating fundraising goals. This ensures community oversight.
On-Chain Transparency: All donations, proposals, votes, and fund withdrawals are recorded as transactions on the blockchain, providing an immutable and publicly verifiable ledger of all activities.

Key Features

For Public Users & Donors
Connect Wallet: Users can connect their Ethereum wallets using MetaMask to interact with the DApp.
Make Donations: Anyone can donate ETH to a registered NGO by providing the NGO's address and a donation amount.
Gain Voting Rights: Upon making their first donation, a user's address is marked as a donor (isDonor), granting them the ability to vote on active proposals.
View Proposals: All users can view the list of active governance proposals, including their descriptions, target NGOs, and current vote counts.
Vote on Proposals: Registered donors can cast votes to either approve or reject active proposals. The interface prevents double-voting.
Explore Platform Data: The portal includes a rich set of features for exploring platform statistics, including a directory of all registered NGOs, an NGO balance checker, fundraising goal progress, a leaderboard of top donors, and a history of all donations.

For Registered NGOs
Withdraw Funds: Registered NGOs can securely withdraw the full balance of donated funds to their wallet from the NGO Control Panel.
Propose Goal Updates: NGOs can submit proposals to the community to update their own fundraising goal amounts.

For the Platform Administrator
Admin Authentication: The dashboard is restricted to the contract owner's address, verified upon wallet connection.
Register First NGO: The admin has the unique ability to register the very first NGO on the platform directly, bootstrapping the system.
Propose New NGOs: After the first NGO is set, the admin can submit proposals to register new NGOs, which must then be approved by community vote.
Manage NGO Status: The admin can create proposals to suspend or reactivate an NGO's status on the platform.
Manage Proposals: The admin can view all active proposals and their voting status.
Execute Proposals: Once a proposal has met the required quorum and has more 'For' votes than 'Against', the admin can execute it, triggering the corresponding on-chain action.
Update Quorum: The admin has the authority to update the number of votes required for a proposal to be considered valid.


Technology Stack
Smart Contract: Solidity 
Frontend: HTML5, CSS3, JavaScript 
Web3 Integration: Ethers.js (v5.7.2) 
Styling & UI: Bootstrap, Bootstrap Icons, Google Fonts (Poppins) 
Local Blockchain: Ganache (for development and testing)

Setup & Usage
To run this project locally, you will need Node.js and a browser with the MetaMask extension.

1. Deploy the Smart Contract: Deploy the CharityDonation.sol contract to a local blockchain network like Ganache.
2. Configure Contract: Update contractConfig.js with the new contract address and ensure the ABI is correct.
3. Serve the Files: Use a local web server to serve the project files (home.html, public.html, admin.html, and the .js files).
4. Interact with the DApp:
    Open home.html to start from the landing page.
    Connect two different accounts in MetaMask: one to act as the Admin (the address that deployed the contract) and another to act as a Donor/NGO.
    Use the Admin Dashboard to register the first NGO.
    Use the Public Portal to donate from the second account, and then use the governance features.
