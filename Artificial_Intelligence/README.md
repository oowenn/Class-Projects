# Usage

Here are a list of commands that run the various agents I implemented. Run the following commands within the /pacman/ directory.

## In valueIterationAgent.py

### Value Iteration

python3 -m pacai.bin.gridworld --agent value --iterations 100 --episodes 10

### Q-learning

python3 -m pacai.bin.gridworld --agent q --episodes 100

python3 -m pacai.bin.crawler

python3 -m pacai.bin.pacman -p PacmanQAgent --num-training 2000 --num-games 2010 --layout smallGrid

### Approximate Q-learning

python3 -m pacai.bin.pacman -p ApproximateQAgent --num-training 2000 --num-games 2010 --layout smallGrid

python3 -m pacai.bin.pacman -p ApproximateQAgent --agent-args extractor=pacai.core.featureExtractors.SimpleExtractor --num-training 50 --num-games 60 --layout mediumGrid

## In multiagents.py

### Minimax

python3 -m pacai.bin.pacman --pacman MinimaxAgent --layout minimaxClassic --agent-args depth=4

python3 -m pacai.bin.pacman --pacman MinimaxAgent --layout smallClassic --agent-args depth=3

### Alpha Beta Pruning Minimax

python3 -m pacai.bin.pacman --pacman AlphaBetaAgent --agent-args depth=3 --layout smallClassic

### Expectimax

python3 -m pacai.bin.pacman --layout smallClassic --pacman ExpectimaxAgent --agent-args evalFn=pacai.student.multiagents.betterEvaluationFunction --null-graphics --num-games 10

## In search.py

### A Star Search

python3 -m pacai.bin.pacman --layout trickySearch --pacman AStarFoodSearchAgent

### Uniform Cost Search

python3 -m pacai.bin.pacman --layout mediumMaze --pacman SearchAgent --agent-args fn=pacai.student.search.uniformCostSearch

python3 -m pacai.bin.pacman --layout mediumDottedMaze --pacman StayEastSearchAgent

python3 -m pacai.bin.pacman --layout mediumScaryMaze --pacman StayWestSearchAgent

### DFS

python3 -m pacai.bin.pacman --layout tinyMaze --pacman SearchAgent --agent-args fn=pacai.student.search.depthFirstSearch

python3 -m pacai.bin.pacman --layout mediumMaze --pacman SearchAgent --agent-args fn=pacai.student.search.depthFirstSearch

python3 -m pacai.bin.pacman --layout bigMaze --pacman SearchAgent --agent-args fn=pacai.student.search.depthFirstSearch

### BFS

python3 -m pacai.bin.pacman --layout mediumMaze --pacman SearchAgent --agent-args fn=pacai.student.search.breadthFirstSearch

python3 -m pacai.bin.pacman --layout bigMaze --pacman SearchAgent --agent-args fn=pacai.student.search.breadthFirstSearch

