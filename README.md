# Autonomous Software Agents Project
This project is part of the "Autonomous Software Agents" course of "Artificial Intelligence Systems" master degree. 

The objective is to develop an autonomous agent based on the Belief-Desire-Intention (BDI) architecture. The agent is designed to play [Deliveroo.js](https://github.com/unitn-ASA/Deliveroo.js.git) game.

## Project Structure
`````
├── Beliefs
│   ├── map.js              # Manage informations about the map
│   ├── beliefs.js          # Manage agent's beliefs
│   └── sensing.js          # Manage agent's perceptions of parcels and other agents 
├── Communication           # Multi-agent mode
│   ├── communication.js    # Manage communication between agents 
│   └── teamOptions.js      # Manage the communication of options between agents
├── deliveroo               # Game configuration
│   ├── client.js
│   └── config.js
├── index.js
├── Intentions
│   ├── intentions.js   # Intention Execution
│   └── options.js      # Compute utility and choose best option
├── main.js
├── Plan
│   ├── astar_search.js # Search algorithm
│   ├── PDDL            # Contain PDDL domain and problem files
│   └── plan.js         # Manage all possible plans
└── utils.js
`````

## Intallation
Clone the repository:
```
git clone https://github.com/MartinaPanini/BDI_Agent.git
``` 
Install dependencies:
``` npm install ``` 
**Setup environment**
In index.js:
``` 
const host = "https://deliveroojs2.rtibdi.disi.unitn.it/";
const mexican = { id: '', name: '', token: '' };
const caravan = { id: '', name: '', token: '' };
```
Set the agent's parameters: id, name and token.
In alternative, you can copy the token in index.js and past in Deliveroo game during the login phase. 

### Running
- Connect the agent(s) in Deliveroo game
- Go inside BDI folder
- Single mode: 
    ``` node index.js single ```
- Multi-mode: 
    ``` node index.js multi ```