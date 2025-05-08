```mermaid
classDiagram
    class Main {
        + main(String[] args) void
    }

    Main --> Tile : uses
    Main --> PathFinder : uses
    Main --> StdDraw : uses
