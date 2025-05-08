```mermaid
classDiagram
    class PathFinder {
        - Tile[][] map
        - Map~String, Double~ travelCosts
        - int cols
        - int rows
        + PathFinder(Tile[][] map, Map~String, Double~ travelCosts)
        + findShortestPath(int[] start, int[] goal) PathResult
    }

    class PathResult {
        + List~int[]~ path
        + double totalCost
        + PathResult(List~int[]~ path, double totalCost)
    }

    class Node {
        + int x
        + int y
        + double cost
        + Node(int x, int y, double cost)
    }

    PathFinder --> PathResult
    PathFinder --> Node
