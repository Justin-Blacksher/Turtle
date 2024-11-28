package Turtle


type Weapon struct {
    Class    string
    Range    int8
    Name     string
}

type Enemy struct {
    Name     string
    Color    string
    x        int8
    y        int8
    Weapon   []Weapon
    Nearby   []Ninja
}

type Ninja struct {
    Name     string
    Color    string
    x        int8
    y        int8
    Weapons  []Weapon
    Nearby   []Enemy
}

type Cell struct {
    ninjas      []Ninja
    enemies     []Enemy
}

type MapLayout struct {
    gridSize    int16
    grid        [][]*Cell
}


// Make Map Functions


func NewMap(gridSize int16) *MapLayout {
    grid := make([][]*Cell, gridSize)
    for i := range grid {
        grid[i] = make([]*Cell, gridSize)
        for j := range grid {
            grid[i][j] = &Cell{
                ninjas:    []Ninja{},
                enemies:   []Enemy{},
            }
        }
    }
    return &MapLayout{gridSize: gridSize, grid: grid}
}

