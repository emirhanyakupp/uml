```mermaid
classDiagram
    class ShortestRoute {
        + findFastRoute(int[] start, List~int[]~ coins, PathFinder pf) FastResult
        + getCoinIndicesInRoute(List~int[]~ route, List~int[]~ originalCoins) List~Integer~
    }

    class FastResult {
        + List~int[]~ coinOrder
        + double totalCost
        + FastResult(List~int[]~ coinOrder, double totalCost)
    }

    ShortestRoute --> FastResult
    ShortestRoute --> PathFinder
