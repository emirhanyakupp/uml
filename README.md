```mermaid
classDiagram
    class Tile {
        - int type
        + Tile(int column, int row, int type)
        + isPassable() boolean
        + getType() int
        + loadMap(String filename) Tile[][]
        + readStartAndCoins(String filename, ArrayList~int[]~ coins) int[]
        + readTravelCosts(String filename) Map~String, Double~
        + drawBaseMap(Tile[][] map, int cols, int rows, ArrayList~int[]~ coins) void
        + drawKnight(int x, int y, int rows) void
        + selectDifferentColor(Random rand, Color currentColor) Color
    }

    class ColoredPoint {
        - int[] point
        - Color color
        + ColoredPoint(int[] point, Color color)
    }

    Tile --> ColoredPoint
    Tile --> StdDraw : uses
