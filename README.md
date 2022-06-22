# Go game engine


## Objective

Validate, process, and score a move on a given board in the game of Go.


## API

### API Input
- N x N matrix where 5 ≤ N ≤ 25 and is odd
    - Represents current board configuration
    - Matrix values are 0,1, or 2
        - 0 means empty
        - 1 means white stone
        - 2 means black stone
- 2D Coordinate pair
    - Represents next move
- One Boolean value
    - Represents color of next move
    - True = White
    - False = Black


### API Output
- If successful
    - Dict with following items
        - N x N matrix with new board configuration
        - Score
- If not succesful
    - Bool False



## Software Components

### Component 1 - Move Validation

#### Task
- Check if given move is allowable on current board
    - No stone there already
    - Does not count as suicide
    - Numbers within range
    - Etc...

#### Assumptions
- May assume existing board is already validated from before


### Component 2 - Stone Capture

#### Task
- Process the new board to determine any stone captures
- Generate a new board

#### Assumptions
- May assume the only captured stones are due to the new piece, if it helps (as earlier board was already valid)


### Component 3 - Score calculator

#### Task
- Score the new board based on the scoring rules of go


## Links

- https://www.cs.cmu.edu/~wjh/go/rules/Chinese.html
- https://www.cs.mcgill.ca/~rwest/wikispeedia/wpcd/wp/g/Go_%2528board_game%2529.htm
