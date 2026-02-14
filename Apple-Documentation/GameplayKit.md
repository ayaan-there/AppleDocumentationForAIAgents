# GameplayKit Documentation

Source: https://sosumi.ai/documentation/gameplaykit

---
title: GameplayKit
source: https://developer.apple.com/documentation/gameplaykit
timestamp: 2026-02-13T18:57:17.446Z
---

## Entities and Components

- [GKEntity](/documentation/gameplaykit/gkentity)

### Creating an Entity

- [init()](/documentation/gameplaykit/gkentity/init())

### Managing an Entity’s List of Components

- [var components: [GKComponent]](/documentation/gameplaykit/gkentity/components)
- [func addComponent(GKComponent)](/documentation/gameplaykit/gkentity/addcomponent(_:))

### Performing Periodic Updates

- [func update(deltaTime: TimeInterval)](/documentation/gameplaykit/gkentity/update(deltatime:))

### Instance Methods

- [func component<ComponentType>(ofType: ComponentType.Type) -> ComponentType?](/documentation/gameplaykit/gkentity/component(oftype:))
- [func removeComponent<ComponentType>(ofType: ComponentType.Type)](/documentation/gameplaykit/gkentity/removecomponent(oftype:))
- [GKComponent](/documentation/gameplaykit/gkcomponent)

### Performing Periodic Updates

- [func update(deltaTime: TimeInterval)](/documentation/gameplaykit/gkcomponent/update(deltatime:))

### Working with Entities

- [var entity: GKEntity?](/documentation/gameplaykit/gkcomponent/entity)
- [func didAddToEntity()](/documentation/gameplaykit/gkcomponent/didaddtoentity())
- [func willRemoveFromEntity()](/documentation/gameplaykit/gkcomponent/willremovefromentity())
- [GKComponentSystem](/documentation/gameplaykit/gkcomponentsystem)

### Creating a Component System

- [init(componentClass: AnyClass)](/documentation/gameplaykit/gkcomponentsystem/init(componentclass:))

### Managing a List of Components

- [var componentClass: AnyClass](/documentation/gameplaykit/gkcomponentsystem/componentclass)
- [var components: [ComponentType]](/documentation/gameplaykit/gkcomponentsystem/components)
- [func addComponent(ComponentType)](/documentation/gameplaykit/gkcomponentsystem/addcomponent(_:))
- [func addComponent(foundIn: GKEntity)](/documentation/gameplaykit/gkcomponentsystem/addcomponent(foundin:))
- [func removeComponent(ComponentType)](/documentation/gameplaykit/gkcomponentsystem/removecomponent(_:))
- [func removeComponent(foundIn: GKEntity)](/documentation/gameplaykit/gkcomponentsystem/removecomponent(foundin:))

### Performing Periodic Updates

- [func update(deltaTime: TimeInterval)](/documentation/gameplaykit/gkcomponentsystem/update(deltatime:))

### Accessing Components With Subscript Syntax

- [subscript(Int) -> ComponentType](/documentation/gameplaykit/gkcomponentsystem/subscript(_:))

### Instance Methods

- [func classForGenericArgument(at: Int) -> AnyClass](/documentation/gameplaykit/gkcomponentsystem/classforgenericargument(at:))

## State Machines

- [GKState](/documentation/gameplaykit/gkstate)

### Creating a State

- [init()](/documentation/gameplaykit/gkstate/init())

### Working with State Machines

- [var stateMachine: GKStateMachine?](/documentation/gameplaykit/gkstate/statemachine)
- [func isValidNextState(AnyClass) -> Bool](/documentation/gameplaykit/gkstate/isvalidnextstate(_:))

### Handling State Transitions and Updates

- [func didEnter(from: GKState?)](/documentation/gameplaykit/gkstate/didenter(from:))
- [func update(deltaTime: TimeInterval)](/documentation/gameplaykit/gkstate/update(deltatime:))
- [func willExit(to: GKState)](/documentation/gameplaykit/gkstate/willexit(to:))
- [GKStateMachine](/documentation/gameplaykit/gkstatemachine)

### Creating a State Machine

- [init(states: [GKState])](/documentation/gameplaykit/gkstatemachine/init(states:))

### Working with States

- [var currentState: GKState?](/documentation/gameplaykit/gkstatemachine/currentstate)
- [func canEnterState(AnyClass) -> Bool](/documentation/gameplaykit/gkstatemachine/canenterstate(_:))
- [func enter(AnyClass) -> Bool](/documentation/gameplaykit/gkstatemachine/enter(_:))
- [func update(deltaTime: TimeInterval)](/documentation/gameplaykit/gkstatemachine/update(deltatime:))

### Instance Methods

- [func state<StateType>(forClass: StateType.Type) -> StateType?](/documentation/gameplaykit/gkstatemachine/state(forclass:))

## Spatial Partitioning

- [GKQuadtree](/documentation/gameplaykit/gkquadtree)

### Creating a Quadtree

- [init(boundingQuad: GKQuad, minimumCellSize: Float)](/documentation/gameplaykit/gkquadtree/init(boundingquad:minimumcellsize:))

### Adding and Removing Elements

- [func add(ElementType, at: vector_float2) -> GKQuadtreeNode](/documentation/gameplaykit/gkquadtree/add(_:at:))
- [func add(ElementType, in: GKQuad) -> GKQuadtreeNode](/documentation/gameplaykit/gkquadtree/add(_:in:))
- [func remove(ElementType, using: GKQuadtreeNode) -> Bool](/documentation/gameplaykit/gkquadtree/remove(_:using:))
- [func remove(ElementType) -> Bool](/documentation/gameplaykit/gkquadtree/remove(_:))

### Searching for Elements

- [func elements(at: vector_float2) -> [ElementType]](/documentation/gameplaykit/gkquadtree/elements(at:))
- [func elements(in: GKQuad) -> [ElementType]](/documentation/gameplaykit/gkquadtree/elements(in:))

### Constants

- [GKQuad](/documentation/gameplaykit/gkquad)

#### Initializers

- [init()](/documentation/gameplaykit/gkquad/init())
- [init(quadMin: vector_float2, quadMax: vector_float2)](/documentation/gameplaykit/gkquad/init(quadmin:quadmax:))

#### Instance Properties

- [var quadMax: vector_float2](/documentation/gameplaykit/gkquad/quadmax)
- [var quadMin: vector_float2](/documentation/gameplaykit/gkquad/quadmin)
- [GKQuadtreeNode](/documentation/gameplaykit/gkquadtreenode)

### Examining a Node

- [var quad: GKQuad](/documentation/gameplaykit/gkquadtreenode/quad)
- [GKOctree](/documentation/gameplaykit/gkoctree)

### Creating an Octree

- [init(boundingBox: GKBox, minimumCellSize: Float)](/documentation/gameplaykit/gkoctree/init(boundingbox:minimumcellsize:))

### Adding and Removing Elements

- [func add(ElementType, at: vector_float3) -> GKOctreeNode](/documentation/gameplaykit/gkoctree/add(_:at:))
- [func add(ElementType, in: GKBox) -> GKOctreeNode](/documentation/gameplaykit/gkoctree/add(_:in:))
- [func remove(ElementType, using: GKOctreeNode) -> Bool](/documentation/gameplaykit/gkoctree/remove(_:using:))
- [func remove(ElementType) -> Bool](/documentation/gameplaykit/gkoctree/remove(_:))

### Searching for Elements

- [func elements(at: vector_float3) -> [ElementType]](/documentation/gameplaykit/gkoctree/elements(at:))
- [func elements(in: GKBox) -> [ElementType]](/documentation/gameplaykit/gkoctree/elements(in:))

### Constants

- [GKBox](/documentation/gameplaykit/gkbox)

#### Initializers

- [init()](/documentation/gameplaykit/gkbox/init())
- [init(boxMin: vector_float3, boxMax: vector_float3)](/documentation/gameplaykit/gkbox/init(boxmin:boxmax:))

#### Instance Properties

- [var boxMax: vector_float3](/documentation/gameplaykit/gkbox/boxmax)
- [var boxMin: vector_float3](/documentation/gameplaykit/gkbox/boxmin)
- [GKOctreeNode](/documentation/gameplaykit/gkoctreenode)

### Examining a Node

- [var box: GKBox](/documentation/gameplaykit/gkoctreenode/box)
- [GKRTree](/documentation/gameplaykit/gkrtree)

### Creating an R-Tree

- [init(maxNumberOfChildren: Int)](/documentation/gameplaykit/gkrtree/init(maxnumberofchildren:))

### Adding and Removing Elements

- [func addElement(ElementType, boundingRectMin: vector_float2, boundingRectMax: vector_float2, splitStrategy: GKRTreeSplitStrategy)](/documentation/gameplaykit/gkrtree/addelement(_:boundingrectmin:boundingrectmax:splitstrategy:))
- [func removeElement(ElementType, boundingRectMin: vector_float2, boundingRectMax: vector_float2)](/documentation/gameplaykit/gkrtree/removeelement(_:boundingrectmin:boundingrectmax:))

### Searching for Elements

- [func elements(inBoundingRectMin: vector_float2, rectMax: vector_float2) -> [ElementType]](/documentation/gameplaykit/gkrtree/elements(inboundingrectmin:rectmax:))
- [var queryReserve: Int](/documentation/gameplaykit/gkrtree/queryreserve)

### Constants

- [GKRTreeSplitStrategy](/documentation/gameplaykit/gkrtreesplitstrategy)

#### Constants

- [case halve](/documentation/gameplaykit/gkrtreesplitstrategy/halve)
- [case linear](/documentation/gameplaykit/gkrtreesplitstrategy/linear)
- [case quadratic](/documentation/gameplaykit/gkrtreesplitstrategy/quadratic)
- [case reduceOverlap](/documentation/gameplaykit/gkrtreesplitstrategy/reduceoverlap)

#### Initializers

- [init?(rawValue: Int)](/documentation/gameplaykit/gkrtreesplitstrategy/init(rawvalue:))

## Strategists

- [GKStrategist](/documentation/gameplaykit/gkstrategist)

### Specifying the Game Model

- [var gameModel: (any GKGameModel)?](/documentation/gameplaykit/gkstrategist/gamemodel)

### Configuring a Strategist

- [var randomSource: (any GKRandom)?](/documentation/gameplaykit/gkstrategist/randomsource)

### Planning Game Moves

- [func bestMoveForActivePlayer() -> (any GKGameModelUpdate)?](/documentation/gameplaykit/gkstrategist/bestmoveforactiveplayer())
- [GKMinmaxStrategist](/documentation/gameplaykit/gkminmaxstrategist)

### Configuring a Strategist

- [var maxLookAheadDepth: Int](/documentation/gameplaykit/gkminmaxstrategist/maxlookaheaddepth)

### Planning Game Moves

- [func bestMove(for: any GKGameModelPlayer) -> (any GKGameModelUpdate)?](/documentation/gameplaykit/gkminmaxstrategist/bestmove(for:))
- [func randomMove(for: any GKGameModelPlayer, fromNumberOfBestMoves: Int) -> (any GKGameModelUpdate)?](/documentation/gameplaykit/gkminmaxstrategist/randommove(for:fromnumberofbestmoves:))
- [GKMonteCarloStrategist](/documentation/gameplaykit/gkmontecarlostrategist)

### Configuring a Strategist

- [var budget: Int](/documentation/gameplaykit/gkmontecarlostrategist/budget)
- [var explorationParameter: Int](/documentation/gameplaykit/gkmontecarlostrategist/explorationparameter)
- [GKGameModel](/documentation/gameplaykit/gkgamemodel)

### Keeping Track of Players

- [var players: [any GKGameModelPlayer]?](/documentation/gameplaykit/gkgamemodel/players)
- [var activePlayer: (any GKGameModelPlayer)?](/documentation/gameplaykit/gkgamemodel/activeplayer)

### Evaluating a Game Model

- [func gameModelUpdates(for: any GKGameModelPlayer) -> [any GKGameModelUpdate]?](/documentation/gameplaykit/gkgamemodel/gamemodelupdates(for:))
- [func score(for: any GKGameModelPlayer) -> Int](/documentation/gameplaykit/gkgamemodel/score(for:))
- [func isLoss(for: any GKGameModelPlayer) -> Bool](/documentation/gameplaykit/gkgamemodel/isloss(for:))
- [func isWin(for: any GKGameModelPlayer) -> Bool](/documentation/gameplaykit/gkgamemodel/iswin(for:))

### Modifying a Game Model

- [func apply(any GKGameModelUpdate)](/documentation/gameplaykit/gkgamemodel/apply(_:))
- [func unapplyGameModelUpdate(any GKGameModelUpdate)](/documentation/gameplaykit/gkgamemodel/unapplygamemodelupdate(_:))
- [func setGameModel(any GKGameModel)](/documentation/gameplaykit/gkgamemodel/setgamemodel(_:))

### Constants

- [Game Model Score Limits](/documentation/gameplaykit/game-model-score-limits)

#### Constants

- [let GKGameModelMaxScore: Int](/documentation/gameplaykit/gkgamemodelmaxscore)
- [let GKGameModelMinScore: Int](/documentation/gameplaykit/gkgamemodelminscore)
- [GKGameModelPlayer](/documentation/gameplaykit/gkgamemodelplayer)

### Identifying a Player

- [var playerId: Int](/documentation/gameplaykit/gkgamemodelplayer/playerid)
- [GKGameModelUpdate](/documentation/gameplaykit/gkgamemodelupdate)

### Storing a Move Value

- [var value: Int](/documentation/gameplaykit/gkgamemodelupdate/value)

## Decision Trees

- [GKDecisionTree](/documentation/gameplaykit/gkdecisiontree)

### Creating a Manually Defined Decision Tree

- [init(attribute: any NSObjectProtocol)](/documentation/gameplaykit/gkdecisiontree/init(attribute:))
- [var rootNode: GKDecisionNode?](/documentation/gameplaykit/gkdecisiontree/rootnode)

### Creating a Learned Decision Tree

- [init(examples: [[any NSObjectProtocol]], actions: [any NSObjectProtocol], attributes: [any NSObjectProtocol])](/documentation/gameplaykit/gkdecisiontree/init(examples:actions:attributes:))

### Evaluating a Tree to Make Decisions

- [func findAction(forAnswers: [AnyHashable : any NSObjectProtocol]) -> (any NSObjectProtocol)?](/documentation/gameplaykit/gkdecisiontree/findaction(foranswers:))
- [var randomSource: GKRandomSource](/documentation/gameplaykit/gkdecisiontree/randomsource)

### Initializers

- [init(url: URL, error: (any Error)?)](/documentation/gameplaykit/gkdecisiontree/init(url:error:))

### Instance Methods

- [func export(to: URL, error: (any Error)?) -> Bool](/documentation/gameplaykit/gkdecisiontree/export(to:error:))
- [GKDecisionNode](/documentation/gameplaykit/gkdecisionnode)

### Creating Child Nodes for Decision Branches

- [func createBranch(value: NSNumber, attribute: any NSObjectProtocol) -> Self](/documentation/gameplaykit/gkdecisionnode/createbranch(value:attribute:))
- [func createBranch(predicate: NSPredicate, attribute: any NSObjectProtocol) -> Self](/documentation/gameplaykit/gkdecisionnode/createbranch(predicate:attribute:))
- [func createBranch(weight: Int, attribute: any NSObjectProtocol) -> Self](/documentation/gameplaykit/gkdecisionnode/createbranch(weight:attribute:))

## Pathfinding

- [GKGraph](/documentation/gameplaykit/gkgraph)

### Creating a Graph

- [init([GKGraphNode])](/documentation/gameplaykit/gkgraph/init(_:))

### Working with Nodes in a Graph

- [func add([GKGraphNode])](/documentation/gameplaykit/gkgraph/add(_:))
- [func connectToLowestCostNode(node: GKGraphNode, bidirectional: Bool)](/documentation/gameplaykit/gkgraph/connecttolowestcostnode(node:bidirectional:))
- [func remove([GKGraphNode])](/documentation/gameplaykit/gkgraph/remove(_:))
- [var nodes: [GKGraphNode]?](/documentation/gameplaykit/gkgraph/nodes)

### Pathfinding with a Graph

- [func findPath(from: GKGraphNode, to: GKGraphNode) -> [GKGraphNode]](/documentation/gameplaykit/gkgraph/findpath(from:to:))
- [GKObstacleGraph](/documentation/gameplaykit/gkobstaclegraph)

### Creating a Graph

- [init(obstacles: [GKPolygonObstacle], bufferRadius: Float, nodeClass: AnyClass)](/documentation/gameplaykit/gkobstaclegraph/init(obstacles:bufferradius:nodeclass:))
- [init(obstacles: [GKPolygonObstacle], bufferRadius: Float)](/documentation/gameplaykit/gkobstaclegraph/init(obstacles:bufferradius:))

### Working with Obstacles

- [var obstacles: [GKPolygonObstacle]](/documentation/gameplaykit/gkobstaclegraph/obstacles)
- [func addObstacles([GKPolygonObstacle])](/documentation/gameplaykit/gkobstaclegraph/addobstacles(_:))
- [func removeObstacles([GKPolygonObstacle])](/documentation/gameplaykit/gkobstaclegraph/removeobstacles(_:))
- [func removeAllObstacles()](/documentation/gameplaykit/gkobstaclegraph/removeallobstacles())
- [func nodes(for: GKPolygonObstacle) -> [NodeType]](/documentation/gameplaykit/gkobstaclegraph/nodes(for:))

### Working with Nodes

- [func connectUsingObstacles(node: NodeType)](/documentation/gameplaykit/gkobstaclegraph/connectusingobstacles(node:))
- [func connectUsingObstacles(node: NodeType, ignoring: [GKPolygonObstacle])](/documentation/gameplaykit/gkobstaclegraph/connectusingobstacles(node:ignoring:))
- [func connectUsingObstacles(node: NodeType, ignoringBufferRadiusOf: [GKPolygonObstacle])](/documentation/gameplaykit/gkobstaclegraph/connectusingobstacles(node:ignoringbufferradiusof:))
- [var bufferRadius: Float](/documentation/gameplaykit/gkobstaclegraph/bufferradius)

### Locking Node Connections

- [func lockConnection(from: NodeType, to: NodeType)](/documentation/gameplaykit/gkobstaclegraph/lockconnection(from:to:))
- [func unlockConnection(from: NodeType, to: NodeType)](/documentation/gameplaykit/gkobstaclegraph/unlockconnection(from:to:))
- [func isConnectionLocked(from: NodeType, to: NodeType) -> Bool](/documentation/gameplaykit/gkobstaclegraph/isconnectionlocked(from:to:))

### Instance Methods

- [func classForGenericArgument(at: Int) -> AnyClass](/documentation/gameplaykit/gkobstaclegraph/classforgenericargument(at:))
- [GKMeshGraph](/documentation/gameplaykit/gkmeshgraph)

### Creating a Graph

- [init(bufferRadius: Float, minCoordinate: vector_float2, maxCoordinate: vector_float2, nodeClass: AnyClass)](/documentation/gameplaykit/gkmeshgraph/init(bufferradius:mincoordinate:maxcoordinate:nodeclass:))
- [init(bufferRadius: Float, minCoordinate: vector_float2, maxCoordinate: vector_float2)](/documentation/gameplaykit/gkmeshgraph/init(bufferradius:mincoordinate:maxcoordinate:))

### Working with Obstacles

- [var obstacles: [GKPolygonObstacle]](/documentation/gameplaykit/gkmeshgraph/obstacles)
- [func addObstacles([GKPolygonObstacle])](/documentation/gameplaykit/gkmeshgraph/addobstacles(_:))
- [func removeObstacles([GKPolygonObstacle])](/documentation/gameplaykit/gkmeshgraph/removeobstacles(_:))

### Working with Nodes

- [func connectUsingObstacles(node: NodeType)](/documentation/gameplaykit/gkmeshgraph/connectusingobstacles(node:))
- [var bufferRadius: Float](/documentation/gameplaykit/gkmeshgraph/bufferradius)

### Managing the Mesh

- [func triangulate()](/documentation/gameplaykit/gkmeshgraph/triangulate())
- [var triangulationMode: GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraph/triangulationmode)
- [func triangle(at: Int) -> GKTriangle](/documentation/gameplaykit/gkmeshgraph/triangle(at:))
- [var triangleCount: Int](/documentation/gameplaykit/gkmeshgraph/trianglecount)

### Constants

- [GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode)

#### Constants

- [static var vertices: GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode/vertices)
- [static var centers: GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode/centers)
- [static var edgeMidpoints: GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode/edgemidpoints)

#### Initializers

- [init(rawValue: UInt)](/documentation/gameplaykit/gkmeshgraphtriangulationmode/init(rawvalue:))
- [GKTriangle](/documentation/gameplaykit/gktriangle)

#### Initializers

- [init()](/documentation/gameplaykit/gktriangle/init())
- [init(points: (vector_float3, vector_float3, vector_float3))](/documentation/gameplaykit/gktriangle/init(points:))

#### Instance Properties

- [var points: (vector_float3, vector_float3, vector_float3)](/documentation/gameplaykit/gktriangle/points)

### Instance Methods

- [func classForGenericArgument(at: Int) -> AnyClass](/documentation/gameplaykit/gkmeshgraph/classforgenericargument(at:))
- [GKGridGraph](/documentation/gameplaykit/gkgridgraph)

### Creating a Graph

- [init(fromGridStartingAt: vector_int2, width: Int32, height: Int32, diagonalsAllowed: Bool, nodeClass: AnyClass)](/documentation/gameplaykit/gkgridgraph/init(fromgridstartingat:width:height:diagonalsallowed:nodeclass:))
- [init(fromGridStartingAt: vector_int2, width: Int32, height: Int32, diagonalsAllowed: Bool)](/documentation/gameplaykit/gkgridgraph/init(fromgridstartingat:width:height:diagonalsallowed:))

### Working with Nodes

- [func node(atGridPosition: vector_int2) -> NodeType?](/documentation/gameplaykit/gkgridgraph/node(atgridposition:))
- [func connectToAdjacentNodes(node: GKGridGraphNode)](/documentation/gameplaykit/gkgridgraph/connecttoadjacentnodes(node:))

### Inspecting a Graph

- [var diagonalsAllowed: Bool](/documentation/gameplaykit/gkgridgraph/diagonalsallowed)
- [var gridOrigin: vector_int2](/documentation/gameplaykit/gkgridgraph/gridorigin)
- [var gridWidth: Int](/documentation/gameplaykit/gkgridgraph/gridwidth)
- [var gridHeight: Int](/documentation/gameplaykit/gkgridgraph/gridheight)

### Instance Methods

- [func classForGenericArgument(at: Int) -> AnyClass](/documentation/gameplaykit/gkgridgraph/classforgenericargument(at:))
- [GKGraphNode](/documentation/gameplaykit/gkgraphnode)

### Working with Connections

- [var connectedNodes: [GKGraphNode]](/documentation/gameplaykit/gkgraphnode/connectednodes)
- [func addConnections(to: [GKGraphNode], bidirectional: Bool)](/documentation/gameplaykit/gkgraphnode/addconnections(to:bidirectional:))
- [func removeConnections(to: [GKGraphNode], bidirectional: Bool)](/documentation/gameplaykit/gkgraphnode/removeconnections(to:bidirectional:))

### Computing Traversal Costs

- [func cost(to: GKGraphNode) -> Float](/documentation/gameplaykit/gkgraphnode/cost(to:))
- [func estimatedCost(to: GKGraphNode) -> Float](/documentation/gameplaykit/gkgraphnode/estimatedcost(to:))

### Finding Paths

- [func findPath(to: GKGraphNode) -> [GKGraphNode]](/documentation/gameplaykit/gkgraphnode/findpath(to:))
- [func findPath(from: GKGraphNode) -> [GKGraphNode]](/documentation/gameplaykit/gkgraphnode/findpath(from:))
- [GKGraphNode2D](/documentation/gameplaykit/gkgraphnode2d)

### Creating a Graph Node

- [init(point: vector_float2)](/documentation/gameplaykit/gkgraphnode2d/init(point:))
- [class func node(withPoint: vector_float2) -> Self](/documentation/gameplaykit/gkgraphnode2d/node(withpoint:))

### Inspecting a Node’s Position

- [var position: vector_float2](/documentation/gameplaykit/gkgraphnode2d/position)
- [GKGraphNode3D](/documentation/gameplaykit/gkgraphnode3d)

### Creating a Graph Node

- [init(point: vector_float3)](/documentation/gameplaykit/gkgraphnode3d/init(point:))
- [class func node(withPoint: vector_float3) -> Self](/documentation/gameplaykit/gkgraphnode3d/node(withpoint:))

### Inspecting a Node’s Position

- [var position: vector_float3](/documentation/gameplaykit/gkgraphnode3d/position)
- [GKGridGraphNode](/documentation/gameplaykit/gkgridgraphnode)

### Creating a Graph Node

- [init(gridPosition: vector_int2)](/documentation/gameplaykit/gkgridgraphnode/init(gridposition:))

### Inspecting a Node’s Position

- [var gridPosition: vector_int2](/documentation/gameplaykit/gkgridgraphnode/gridposition)

## Agents, Goals, and Behaviors

- [GKAgent](/documentation/gameplaykit/gkagent)

### Defining an Agent’s Behavior

- [var behavior: GKBehavior?](/documentation/gameplaykit/gkagent/behavior)

### Constraining an Agent’s Movement

- [var mass: Float](/documentation/gameplaykit/gkagent/mass)
- [var maxAcceleration: Float](/documentation/gameplaykit/gkagent/maxacceleration)
- [var maxSpeed: Float](/documentation/gameplaykit/gkagent/maxspeed)
- [var radius: Float](/documentation/gameplaykit/gkagent/radius)

### Synchronizing an Agent’s Visual Representation

- [var delegate: (any GKAgentDelegate)?](/documentation/gameplaykit/gkagent/delegate)

### Managing an Agent’s Attributes

- [var speed: Float](/documentation/gameplaykit/gkagent/speed)
- [GKAgent2D](/documentation/gameplaykit/gkagent2d)

### Managing an Agent’s Position and Orientation

- [var position: vector_float2](/documentation/gameplaykit/gkagent2d/position)
- [var rotation: Float](/documentation/gameplaykit/gkagent2d/rotation)

### Running the Agent Simulation

- [func update(deltaTime: TimeInterval)](/documentation/gameplaykit/gkagent2d/update(deltatime:))
- [var velocity: vector_float2](/documentation/gameplaykit/gkagent2d/velocity)
- [GKAgent3D](/documentation/gameplaykit/gkagent3d)

### Managing an Agent’s Position and Orientation

- [var position: vector_float3](/documentation/gameplaykit/gkagent3d/position)
- [var rotation: matrix_float3x3](/documentation/gameplaykit/gkagent3d/rotation)

### Running the Agent Simulation

- [func update(deltaTime: TimeInterval)](/documentation/gameplaykit/gkagent3d/update(deltatime:))
- [var velocity: vector_float3](/documentation/gameplaykit/gkagent3d/velocity)

### Instance Properties

- [var rightHanded: Bool](/documentation/gameplaykit/gkagent3d/righthanded)
- [GKGoal](/documentation/gameplaykit/gkgoal)

### Creating Goals for General Movement Behavior

- [convenience init(toSeekAgent: GKAgent)](/documentation/gameplaykit/gkgoal/init(toseekagent:))
- [convenience init(toFleeAgent: GKAgent)](/documentation/gameplaykit/gkgoal/init(tofleeagent:))
- [convenience init(toReachTargetSpeed: Float)](/documentation/gameplaykit/gkgoal/init(toreachtargetspeed:))
- [convenience init(toWander: Float)](/documentation/gameplaykit/gkgoal/init(towander:))

### Creating Goals for Avoidance and Interception Behavior

- [convenience init(toAvoid: [GKAgent], maxPredictionTime: TimeInterval)](/documentation/gameplaykit/gkgoal/init(toavoid:maxpredictiontime:)-96a0i)
- [convenience init(toAvoid: [GKObstacle], maxPredictionTime: TimeInterval)](/documentation/gameplaykit/gkgoal/init(toavoid:maxpredictiontime:)-7oslq)
- [convenience init(toInterceptAgent: GKAgent, maxPredictionTime: TimeInterval)](/documentation/gameplaykit/gkgoal/init(tointerceptagent:maxpredictiontime:))

### Creating Goals for Flocking Behavior

- [convenience init(toSeparateFrom: [GKAgent], maxDistance: Float, maxAngle: Float)](/documentation/gameplaykit/gkgoal/init(toseparatefrom:maxdistance:maxangle:))
- [convenience init(toAlignWith: [GKAgent], maxDistance: Float, maxAngle: Float)](/documentation/gameplaykit/gkgoal/init(toalignwith:maxdistance:maxangle:))
- [convenience init(toCohereWith: [GKAgent], maxDistance: Float, maxAngle: Float)](/documentation/gameplaykit/gkgoal/init(tocoherewith:maxdistance:maxangle:))

### Creating Goals for Path-Following Behavior

- [convenience init(toStayOn: GKPath, maxPredictionTime: TimeInterval)](/documentation/gameplaykit/gkgoal/init(tostayon:maxpredictiontime:))
- [convenience init(toFollow: GKPath, maxPredictionTime: TimeInterval, forward: Bool)](/documentation/gameplaykit/gkgoal/init(tofollow:maxpredictiontime:forward:))
- [GKBehavior](/documentation/gameplaykit/gkbehavior)

### Creating a Behavior

- [convenience init(goal: GKGoal, weight: Float)](/documentation/gameplaykit/gkbehavior/init(goal:weight:))
- [convenience init(goals: [GKGoal])](/documentation/gameplaykit/gkbehavior/init(goals:))
- [convenience init(goals: [GKGoal], andWeights: [NSNumber])](/documentation/gameplaykit/gkbehavior/init(goals:andweights:))
- [convenience init(weightedGoals: [GKGoal : NSNumber])](/documentation/gameplaykit/gkbehavior/init(weightedgoals:))

### Managing a Behavior’s Set of Goals

- [func setWeight(Float, for: GKGoal)](/documentation/gameplaykit/gkbehavior/setweight(_:for:))
- [func weight(for: GKGoal) -> Float](/documentation/gameplaykit/gkbehavior/weight(for:))
- [func remove(GKGoal)](/documentation/gameplaykit/gkbehavior/remove(_:))
- [func removeAllGoals()](/documentation/gameplaykit/gkbehavior/removeallgoals())
- [var goalCount: Int](/documentation/gameplaykit/gkbehavior/goalcount)

### Working with Goals Using Subscript Syntax

- [subscript(GKGoal) -> NSNumber!](/documentation/gameplaykit/gkbehavior/subscript(_:)-2yvko)
- [subscript(Int) -> GKGoal](/documentation/gameplaykit/gkbehavior/subscript(_:)-997a9)
- [GKCompositeBehavior](/documentation/gameplaykit/gkcompositebehavior)

### Creating a Composite Behavior

- [convenience init(behaviors: [GKBehavior])](/documentation/gameplaykit/gkcompositebehavior/init(behaviors:))
- [convenience init(behaviors: [GKBehavior], andWeights: [NSNumber])](/documentation/gameplaykit/gkcompositebehavior/init(behaviors:andweights:))

### Managing the Individual Behaviors in a Composite Behavior

- [func setWeight(Float, for: GKBehavior)](/documentation/gameplaykit/gkcompositebehavior/setweight(_:for:))
- [func weight(for: GKBehavior) -> Float](/documentation/gameplaykit/gkcompositebehavior/weight(for:))
- [func remove(GKBehavior)](/documentation/gameplaykit/gkcompositebehavior/remove(_:))
- [func removeAllBehaviors()](/documentation/gameplaykit/gkcompositebehavior/removeallbehaviors())
- [var behaviorCount: Int](/documentation/gameplaykit/gkcompositebehavior/behaviorcount)

### Working with Behaviors Using Subscript Syntax

- [subscript(GKBehavior) -> NSNumber](/documentation/gameplaykit/gkcompositebehavior/subscript(_:)-6jng9)
- [subscript(Int) -> GKBehavior](/documentation/gameplaykit/gkcompositebehavior/subscript(_:)-6krdg)
- [GKPath](/documentation/gameplaykit/gkpath)

### Creating a Path

- [init(graphNodes: [GKGraphNode], radius: Float)](/documentation/gameplaykit/gkpath/init(graphnodes:radius:))

### Managing a Path’s Attributes

- [var radius: Float](/documentation/gameplaykit/gkpath/radius)
- [var isCyclical: Bool](/documentation/gameplaykit/gkpath/iscyclical)

### Inspecting a Path’s Shape

- [var numPoints: Int](/documentation/gameplaykit/gkpath/numpoints)
- [func float2(at: Int) -> vector_float2](/documentation/gameplaykit/gkpath/float2(at:))
- [func float3(at: Int) -> vector_float3](/documentation/gameplaykit/gkpath/float3(at:))
- [func point(at: Int) -> vector_float2](/documentation/gameplaykit/gkpath/point(at:))

### Initializers

- [convenience init(points: [SIMD3<Float>], radius: Float, cyclical: Bool)](/documentation/gameplaykit/gkpath/init(points:radius:cyclical:)-6qqn4)
- [convenience init(points: [SIMD2<Float>], radius: Float, cyclical: Bool)](/documentation/gameplaykit/gkpath/init(points:radius:cyclical:)-2iv4v)
- [GKAgentDelegate](/documentation/gameplaykit/gkagentdelegate)

### Synchronizing with Agents

- [func agentWillUpdate(GKAgent)](/documentation/gameplaykit/gkagentdelegate/agentwillupdate(_:))
- [func agentDidUpdate(GKAgent)](/documentation/gameplaykit/gkagentdelegate/agentdidupdate(_:))

## Obstacles

- [GKObstacle](/documentation/gameplaykit/gkobstacle)
- [GKCircleObstacle](/documentation/gameplaykit/gkcircleobstacle)

### Creating an Obstacle

- [init(radius: Float)](/documentation/gameplaykit/gkcircleobstacle/init(radius:))

### Placing an Obstacle

- [var position: vector_float2](/documentation/gameplaykit/gkcircleobstacle/position)
- [var radius: Float](/documentation/gameplaykit/gkcircleobstacle/radius)
- [GKSphereObstacle](/documentation/gameplaykit/gksphereobstacle)

### Creating an Obstacle

- [init(radius: Float)](/documentation/gameplaykit/gksphereobstacle/init(radius:))

### Placing an Obstacle

- [var position: vector_float3](/documentation/gameplaykit/gksphereobstacle/position)
- [var radius: Float](/documentation/gameplaykit/gksphereobstacle/radius)
- [GKPolygonObstacle](/documentation/gameplaykit/gkpolygonobstacle)

### Inspecting Vertices

- [var vertexCount: Int](/documentation/gameplaykit/gkpolygonobstacle/vertexcount)
- [func vertex(at: Int) -> vector_float2](/documentation/gameplaykit/gkpolygonobstacle/vertex(at:))

### Initializers

- [convenience init(points: [SIMD2<Float>])](/documentation/gameplaykit/gkpolygonobstacle/init(points:))

## Procedural Noise

- [GKNoiseSource](/documentation/gameplaykit/gknoisesource)
- [GKNoise](/documentation/gameplaykit/gknoise)

### Creating Noise

- [convenience init(GKNoiseSource)](/documentation/gameplaykit/gknoise/init(_:))
- [init(GKNoiseSource, gradientColors: [NSNumber : UIColor])](/documentation/gameplaykit/gknoise/init(_:gradientcolors:))

### Creating Noise by Combining Noise

- [convenience init(componentNoises: [GKNoise], selectionNoise: GKNoise)](/documentation/gameplaykit/gknoise/init(componentnoises:selectionnoise:))
- [convenience init(componentNoises: [GKNoise], selectionNoise: GKNoise, componentBoundaries: [NSNumber], boundaryBlendDistances: [NSNumber])](/documentation/gameplaykit/gknoise/init(componentnoises:selectionnoise:componentboundaries:boundaryblenddistances:))

### Colorizing Noise

- [var gradientColors: [NSNumber : UIColor]](/documentation/gameplaykit/gknoise/gradientcolors)

### Applying Operations to Noise Values

- [func applyAbsoluteValue()](/documentation/gameplaykit/gknoise/applyabsolutevalue())
- [func invert()](/documentation/gameplaykit/gknoise/invert())
- [func raiseToPower(Double)](/documentation/gameplaykit/gknoise/raisetopower(_:)-14715)
- [func clamp(lowerBound: Double, upperBound: Double)](/documentation/gameplaykit/gknoise/clamp(lowerbound:upperbound:))
- [func remapValues(toCurveWithControlPoints: [NSNumber : NSNumber])](/documentation/gameplaykit/gknoise/remapvalues(tocurvewithcontrolpoints:))
- [func remapValues(toTerracesWithPeaks: [NSNumber], terracesInverted: Bool)](/documentation/gameplaykit/gknoise/remapvalues(toterraceswithpeaks:terracesinverted:))

### Applying Operations that Combine Noise

- [func add(GKNoise)](/documentation/gameplaykit/gknoise/add(_:))
- [func multiply(GKNoise)](/documentation/gameplaykit/gknoise/multiply(_:))
- [func raiseToPower(GKNoise)](/documentation/gameplaykit/gknoise/raisetopower(_:)-zm5g)
- [func maximum(GKNoise)](/documentation/gameplaykit/gknoise/maximum(_:))
- [func minimum(GKNoise)](/documentation/gameplaykit/gknoise/minimum(_:))

### Applying Operations that Distort Noise

- [func displaceWithNoises(x: GKNoise, y: GKNoise, z: GKNoise)](/documentation/gameplaykit/gknoise/displacewithnoises(x:y:z:))
- [func applyTurbulence(frequency: Double, power: Double, roughness: Int32, seed: Int32)](/documentation/gameplaykit/gknoise/applyturbulence(frequency:power:roughness:seed:))

### Applying Geometric Transformations

- [func move(by: vector_double3)](/documentation/gameplaykit/gknoise/move(by:))
- [func rotate(by: vector_double3)](/documentation/gameplaykit/gknoise/rotate(by:))
- [func scale(by: vector_double3)](/documentation/gameplaykit/gknoise/scale(by:))

### Initializers

- [convenience init()](/documentation/gameplaykit/gknoise/init())

### Instance Methods

- [func value(atPosition: vector_float2) -> Float](/documentation/gameplaykit/gknoise/value(atposition:))
- [GKNoiseMap](/documentation/gameplaykit/gknoisemap)

### Creating a Noise Map

- [convenience init(GKNoise)](/documentation/gameplaykit/gknoisemap/init(_:))
- [init(GKNoise, size: vector_double2, origin: vector_double2, sampleCount: vector_int2, seamless: Bool)](/documentation/gameplaykit/gknoisemap/init(_:size:origin:samplecount:seamless:))
- [convenience init()](/documentation/gameplaykit/gknoisemap/init())

### Accessing Noise Values

- [func value(at: vector_int2) -> Float](/documentation/gameplaykit/gknoisemap/value(at:))
- [func interpolatedValue(at: vector_float2) -> Float](/documentation/gameplaykit/gknoisemap/interpolatedvalue(at:))
- [func setValue(Float, at: vector_int2)](/documentation/gameplaykit/gknoisemap/setvalue(_:at:))

### Inspecting a Noise Map

- [var size: vector_double2](/documentation/gameplaykit/gknoisemap/size)
- [var origin: vector_double2](/documentation/gameplaykit/gknoisemap/origin)
- [var sampleCount: vector_int2](/documentation/gameplaykit/gknoisemap/samplecount)
- [var isSeamless: Bool](/documentation/gameplaykit/gknoisemap/isseamless)
- [GKCoherentNoiseSource](/documentation/gameplaykit/gkcoherentnoisesource)

### Managing Noise Generation Parameters

- [var frequency: Double](/documentation/gameplaykit/gkcoherentnoisesource/frequency)
- [var octaveCount: Int](/documentation/gameplaykit/gkcoherentnoisesource/octavecount)
- [var lacunarity: Double](/documentation/gameplaykit/gkcoherentnoisesource/lacunarity)
- [var seed: Int32](/documentation/gameplaykit/gkcoherentnoisesource/seed)
- [GKBillowNoiseSource](/documentation/gameplaykit/gkbillownoisesource)

### Creating a Noise Source

- [init(frequency: Double, octaveCount: Int, persistence: Double, lacunarity: Double, seed: Int32)](/documentation/gameplaykit/gkbillownoisesource/init(frequency:octavecount:persistence:lacunarity:seed:))
- [var persistence: Double](/documentation/gameplaykit/gkbillownoisesource/persistence)
- [GKPerlinNoiseSource](/documentation/gameplaykit/gkperlinnoisesource)

### Creating a Noise Source

- [init(frequency: Double, octaveCount: Int, persistence: Double, lacunarity: Double, seed: Int32)](/documentation/gameplaykit/gkperlinnoisesource/init(frequency:octavecount:persistence:lacunarity:seed:))

### Managing Noise Generation Parameters

- [var persistence: Double](/documentation/gameplaykit/gkperlinnoisesource/persistence)
- [GKRidgedNoiseSource](/documentation/gameplaykit/gkridgednoisesource)

### Creating a Noise Source

- [init(frequency: Double, octaveCount: Int, lacunarity: Double, seed: Int32)](/documentation/gameplaykit/gkridgednoisesource/init(frequency:octavecount:lacunarity:seed:))
- [GKVoronoiNoiseSource](/documentation/gameplaykit/gkvoronoinoisesource)

### Creating a Noise Source

- [init(frequency: Double, displacement: Double, distanceEnabled: Bool, seed: Int32)](/documentation/gameplaykit/gkvoronoinoisesource/init(frequency:displacement:distanceenabled:seed:))
- [class func voronoiNoise(withFrequency: Double, displacement: Double, distanceEnabled: Bool, seed: Int32) -> Self](/documentation/gameplaykit/gkvoronoinoisesource/voronoinoise(withfrequency:displacement:distanceenabled:seed:))

### Managing Noise Generation Parameters

- [var frequency: Double](/documentation/gameplaykit/gkvoronoinoisesource/frequency)
- [var displacement: Double](/documentation/gameplaykit/gkvoronoinoisesource/displacement)
- [var isDistanceEnabled: Bool](/documentation/gameplaykit/gkvoronoinoisesource/isdistanceenabled)
- [var seed: Int32](/documentation/gameplaykit/gkvoronoinoisesource/seed)
- [GKCylindersNoiseSource](/documentation/gameplaykit/gkcylindersnoisesource)

### Creating a Noise Source

- [init(frequency: Double)](/documentation/gameplaykit/gkcylindersnoisesource/init(frequency:))
- [class func cylindersNoise(withFrequency: Double) -> Self](/documentation/gameplaykit/gkcylindersnoisesource/cylindersnoise(withfrequency:))

### Managing Noise Generation Parameters

- [var frequency: Double](/documentation/gameplaykit/gkcylindersnoisesource/frequency)
- [GKSpheresNoiseSource](/documentation/gameplaykit/gkspheresnoisesource)

### Creating a Noise Source

- [init(frequency: Double)](/documentation/gameplaykit/gkspheresnoisesource/init(frequency:))
- [class func spheresNoise(withFrequency: Double) -> Self](/documentation/gameplaykit/gkspheresnoisesource/spheresnoise(withfrequency:))

### Managing Noise Generation Parameters

- [var frequency: Double](/documentation/gameplaykit/gkspheresnoisesource/frequency)
- [GKCheckerboardNoiseSource](/documentation/gameplaykit/gkcheckerboardnoisesource)

### Creating a Noise Source

- [init(squareSize: Double)](/documentation/gameplaykit/gkcheckerboardnoisesource/init(squaresize:))
- [class func checkerboardNoise(withSquareSize: Double) -> Self](/documentation/gameplaykit/gkcheckerboardnoisesource/checkerboardnoise(withsquaresize:))

### Managing Noise Generation Parameters

- [var squareSize: Double](/documentation/gameplaykit/gkcheckerboardnoisesource/squaresize)
- [GKConstantNoiseSource](/documentation/gameplaykit/gkconstantnoisesource)

### Creating a Noise Source

- [init(value: Double)](/documentation/gameplaykit/gkconstantnoisesource/init(value:))
- [class func constantNoise(withValue: Double) -> Self](/documentation/gameplaykit/gkconstantnoisesource/constantnoise(withvalue:))

### Managing Noise Generation Parameters

- [var value: Double](/documentation/gameplaykit/gkconstantnoisesource/value)

## Randomization

- [GKRandom](/documentation/gameplaykit/gkrandom)

### Generating Random Numbers

- [func nextInt() -> Int](/documentation/gameplaykit/gkrandom/nextint())
- [func nextInt(upperBound: Int) -> Int](/documentation/gameplaykit/gkrandom/nextint(upperbound:))
- [func nextUniform() -> Float](/documentation/gameplaykit/gkrandom/nextuniform())
- [func nextBool() -> Bool](/documentation/gameplaykit/gkrandom/nextbool())
- [GKRandomSource](/documentation/gameplaykit/gkrandomsource)

### Creating an Independent Random Source

- [init()](/documentation/gameplaykit/gkrandomsource/init())

### Randomly Shuffling an Array

- [func arrayByShufflingObjects(in: [Any]) -> [Any]](/documentation/gameplaykit/gkrandomsource/arraybyshufflingobjects(in:))

### Using a Shared Random Source

- [class func sharedRandom() -> GKRandomSource](/documentation/gameplaykit/gkrandomsource/sharedrandom())

### Initializers

- [init(coder: NSCoder)](/documentation/gameplaykit/gkrandomsource/init(coder:))
- [GKARC4RandomSource](/documentation/gameplaykit/gkarc4randomsource)

### Creating a Random Source

- [convenience init()](/documentation/gameplaykit/gkarc4randomsource/init())
- [init(seed: Data)](/documentation/gameplaykit/gkarc4randomsource/init(seed:))

### Replicating Random Behavior

- [var seed: Data](/documentation/gameplaykit/gkarc4randomsource/seed)

### Avoiding Predictable Behavior

- [func dropValues(Int)](/documentation/gameplaykit/gkarc4randomsource/dropvalues(_:))
- [GKLinearCongruentialRandomSource](/documentation/gameplaykit/gklinearcongruentialrandomsource)

### Creating a Random Source

- [convenience init()](/documentation/gameplaykit/gklinearcongruentialrandomsource/init())
- [init(seed: UInt64)](/documentation/gameplaykit/gklinearcongruentialrandomsource/init(seed:))

### Replicating Random Behavior

- [var seed: UInt64](/documentation/gameplaykit/gklinearcongruentialrandomsource/seed)
- [GKMersenneTwisterRandomSource](/documentation/gameplaykit/gkmersennetwisterrandomsource)

### Creating a Random Source

- [convenience init()](/documentation/gameplaykit/gkmersennetwisterrandomsource/init())
- [init(seed: UInt64)](/documentation/gameplaykit/gkmersennetwisterrandomsource/init(seed:))

### Replicating Random Behavior

- [var seed: UInt64](/documentation/gameplaykit/gkmersennetwisterrandomsource/seed)
- [GKRandomDistribution](/documentation/gameplaykit/gkrandomdistribution)

### Creating a Random Distribution

- [init(randomSource: any GKRandom, lowestValue: Int, highestValue: Int)](/documentation/gameplaykit/gkrandomdistribution/init(randomsource:lowestvalue:highestvalue:))
- [convenience init(lowestValue: Int, highestValue: Int)](/documentation/gameplaykit/gkrandomdistribution/init(lowestvalue:highestvalue:))

### Creating Specific Random Distributions

- [class func d6() -> Self](/documentation/gameplaykit/gkrandomdistribution/d6())
- [class func d20() -> Self](/documentation/gameplaykit/gkrandomdistribution/d20())
- [convenience init(forDieWithSideCount: Int)](/documentation/gameplaykit/gkrandomdistribution/init(fordiewithsidecount:))

### Generating Random Numbers

- [func nextInt() -> Int](/documentation/gameplaykit/gkrandomdistribution/nextint())
- [func nextInt(upperBound: Int) -> Int](/documentation/gameplaykit/gkrandomdistribution/nextint(upperbound:))
- [func nextUniform() -> Float](/documentation/gameplaykit/gkrandomdistribution/nextuniform())
- [func nextBool() -> Bool](/documentation/gameplaykit/gkrandomdistribution/nextbool())

### Working with Characteristics of a Distribution

- [var lowestValue: Int](/documentation/gameplaykit/gkrandomdistribution/lowestvalue)
- [var highestValue: Int](/documentation/gameplaykit/gkrandomdistribution/highestvalue)
- [var numberOfPossibleOutcomes: Int](/documentation/gameplaykit/gkrandomdistribution/numberofpossibleoutcomes)
- [GKGaussianDistribution](/documentation/gameplaykit/gkgaussiandistribution)

### Creating a Random Distribution

- [init(randomSource: any GKRandom, lowestValue: Int, highestValue: Int)](/documentation/gameplaykit/gkgaussiandistribution/init(randomsource:lowestvalue:highestvalue:))
- [init(randomSource: any GKRandom, mean: Float, deviation: Float)](/documentation/gameplaykit/gkgaussiandistribution/init(randomsource:mean:deviation:))

### Working with Characteristics of a Distribution

- [var mean: Float](/documentation/gameplaykit/gkgaussiandistribution/mean)
- [var deviation: Float](/documentation/gameplaykit/gkgaussiandistribution/deviation)
- [GKShuffledDistribution](/documentation/gameplaykit/gkshuffleddistribution)

## Rule Systems

- [GKRule](/documentation/gameplaykit/gkrule)

### Creating Data-Driven Rules

- [convenience init(predicate: NSPredicate, assertingFact: any NSObjectProtocol, grade: Float)](/documentation/gameplaykit/gkrule/init(predicate:assertingfact:grade:))
- [convenience init(predicate: NSPredicate, retractingFact: any NSObjectProtocol, grade: Float)](/documentation/gameplaykit/gkrule/init(predicate:retractingfact:grade:))

### Creating Block-Based Rules

- [convenience init(blockPredicate: (GKRuleSystem) -> Bool, action: (GKRuleSystem) -> Void)](/documentation/gameplaykit/gkrule/init(blockpredicate:action:))

### Setting the Order of Rules in a Rule System

- [var salience: Int](/documentation/gameplaykit/gkrule/salience)

### Evaluating a Rule

- [func evaluatePredicate(in: GKRuleSystem) -> Bool](/documentation/gameplaykit/gkrule/evaluatepredicate(in:))
- [func performAction(in: GKRuleSystem)](/documentation/gameplaykit/gkrule/performaction(in:))
- [GKNSPredicateRule](/documentation/gameplaykit/gknspredicaterule)

### Creating a Predicate-Based Rule

- [init(predicate: NSPredicate)](/documentation/gameplaykit/gknspredicaterule/init(predicate:))

### Evaluating a Rule

- [var predicate: NSPredicate](/documentation/gameplaykit/gknspredicaterule/predicate)
- [func evaluatePredicate(in: GKRuleSystem) -> Bool](/documentation/gameplaykit/gknspredicaterule/evaluatepredicate(in:))
- [GKRuleSystem](/documentation/gameplaykit/gkrulesystem)

### Creating a Rule System

- [init()](/documentation/gameplaykit/gkrulesystem/init())

### Managing State Information

- [var state: NSMutableDictionary](/documentation/gameplaykit/gkrulesystem/state)

### Managing a System’s List of Rules

- [var rules: [GKRule]](/documentation/gameplaykit/gkrulesystem/rules)
- [func add(GKRule)](/documentation/gameplaykit/gkrulesystem/add(_:)-76jb5)
- [func add([GKRule])](/documentation/gameplaykit/gkrulesystem/add(_:)-7u5zw)
- [func removeAllRules()](/documentation/gameplaykit/gkrulesystem/removeallrules())

### Evaluating a Rule System

- [func evaluate()](/documentation/gameplaykit/gkrulesystem/evaluate())
- [var agenda: [GKRule]](/documentation/gameplaykit/gkrulesystem/agenda)
- [var executed: [GKRule]](/documentation/gameplaykit/gkrulesystem/executed)
- [func reset()](/documentation/gameplaykit/gkrulesystem/reset())

### Asserting and Retracting Facts

- [var facts: [Any]](/documentation/gameplaykit/gkrulesystem/facts)
- [func assertFact(any NSObjectProtocol)](/documentation/gameplaykit/gkrulesystem/assertfact(_:))
- [func assertFact(any NSObjectProtocol, grade: Float)](/documentation/gameplaykit/gkrulesystem/assertfact(_:grade:))
- [func retractFact(any NSObjectProtocol)](/documentation/gameplaykit/gkrulesystem/retractfact(_:))
- [func retractFact(any NSObjectProtocol, grade: Float)](/documentation/gameplaykit/gkrulesystem/retractfact(_:grade:))

### Drawing Conclusions from Facts

- [func grade(forFact: any NSObjectProtocol) -> Float](/documentation/gameplaykit/gkrulesystem/grade(forfact:))
- [func minimumGrade(forFacts: [Any]) -> Float](/documentation/gameplaykit/gkrulesystem/minimumgrade(forfacts:))
- [func maximumGrade(forFacts: [Any]) -> Float](/documentation/gameplaykit/gkrulesystem/maximumgrade(forfacts:))

## Xcode and SpriteKit Integration

- [GKScene](/documentation/gameplaykit/gkscene)

### Loading a Scene File

- [convenience init?(fileNamed: String)](/documentation/gameplaykit/gkscene/init(filenamed:))

### Accessing the SpriteKit Scene

- [var rootNode: (any GKSceneRootNodeType)?](/documentation/gameplaykit/gkscene/rootnode)

### Managing Entities and Components

- [var entities: [GKEntity]](/documentation/gameplaykit/gkscene/entities)
- [func addEntity(GKEntity)](/documentation/gameplaykit/gkscene/addentity(_:))
- [func removeEntity(GKEntity)](/documentation/gameplaykit/gkscene/removeentity(_:))

### Managing Pathfinding Graphs

- [var graphs: [String : GKGraph]](/documentation/gameplaykit/gkscene/graphs)
- [func removeGraph(String)](/documentation/gameplaykit/gkscene/removegraph(_:))

### Initializers

- [convenience init?(fileNamed: String, rootNode: any GKSceneRootNodeType)](/documentation/gameplaykit/gkscene/init(filenamed:rootnode:))

### Instance Methods

- [func addGraph(GKGraph, name: String)](/documentation/gameplaykit/gkscene/addgraph(_:name:))
- [GKSceneRootNodeType](/documentation/gameplaykit/gkscenerootnodetype)
- [GKSKNodeComponent](/documentation/gameplaykit/gksknodecomponent)

### Creating a SpriteKit Component

- [init(node: SKNode)](/documentation/gameplaykit/gksknodecomponent/init(node:))

### Accessing the Component’s SpriteKit Node

- [var node: SKNode](/documentation/gameplaykit/gksknodecomponent/node)

## Reference

- [GameplayKit Constants](/documentation/gameplaykit/gameplaykit-constants)

### Constants

- [let GKGameModelMaxScore: Int](/documentation/gameplaykit/gkgamemodelmaxscore)
- [let GKGameModelMinScore: Int](/documentation/gameplaykit/gkgamemodelminscore)

### Macros

- [var GK_VERSION: Int32](/documentation/gameplaykit/gk_version)
- [GameplayKit Structures](/documentation/gameplaykit/gameplaykit-structures)

### Structures

- [GKBox](/documentation/gameplaykit/gkbox)

#### Initializers

- [init()](/documentation/gameplaykit/gkbox/init())
- [init(boxMin: vector_float3, boxMax: vector_float3)](/documentation/gameplaykit/gkbox/init(boxmin:boxmax:))

#### Instance Properties

- [var boxMax: vector_float3](/documentation/gameplaykit/gkbox/boxmax)
- [var boxMin: vector_float3](/documentation/gameplaykit/gkbox/boxmin)
- [GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode)

#### Constants

- [static var vertices: GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode/vertices)
- [static var centers: GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode/centers)
- [static var edgeMidpoints: GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode/edgemidpoints)

#### Initializers

- [init(rawValue: UInt)](/documentation/gameplaykit/gkmeshgraphtriangulationmode/init(rawvalue:))
- [GKQuad](/documentation/gameplaykit/gkquad)

#### Initializers

- [init()](/documentation/gameplaykit/gkquad/init())
- [init(quadMin: vector_float2, quadMax: vector_float2)](/documentation/gameplaykit/gkquad/init(quadmin:quadmax:))

#### Instance Properties

- [var quadMax: vector_float2](/documentation/gameplaykit/gkquad/quadmax)
- [var quadMin: vector_float2](/documentation/gameplaykit/gkquad/quadmin)
- [GKTriangle](/documentation/gameplaykit/gktriangle)

#### Initializers

- [init()](/documentation/gameplaykit/gktriangle/init())
- [init(points: (vector_float3, vector_float3, vector_float3))](/documentation/gameplaykit/gktriangle/init(points:))

#### Instance Properties

- [var points: (vector_float3, vector_float3, vector_float3)](/documentation/gameplaykit/gktriangle/points)
- [GameplayKit Enumerations](/documentation/gameplaykit/gameplaykit-enumerations)

### Enumerations

- [GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode)

#### Constants

- [static var vertices: GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode/vertices)
- [static var centers: GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode/centers)
- [static var edgeMidpoints: GKMeshGraphTriangulationMode](/documentation/gameplaykit/gkmeshgraphtriangulationmode/edgemidpoints)

#### Initializers

- [init(rawValue: UInt)](/documentation/gameplaykit/gkmeshgraphtriangulationmode/init(rawvalue:))
- [GKRTreeSplitStrategy](/documentation/gameplaykit/gkrtreesplitstrategy)

#### Constants

- [case halve](/documentation/gameplaykit/gkrtreesplitstrategy/halve)
- [case linear](/documentation/gameplaykit/gkrtreesplitstrategy/linear)
- [case quadratic](/documentation/gameplaykit/gkrtreesplitstrategy/quadratic)
- [case reduceOverlap](/documentation/gameplaykit/gkrtreesplitstrategy/reduceoverlap)

#### Initializers

- [init?(rawValue: Int)](/documentation/gameplaykit/gkrtreesplitstrategy/init(rawvalue:))

## Classes

- [GKSCNNodeComponent](/documentation/gameplaykit/gkscnnodecomponent)

### Initializers

- [init(node: SCNNode)](/documentation/gameplaykit/gkscnnodecomponent/init(node:))

### Instance Properties

- [var node: SCNNode](/documentation/gameplaykit/gkscnnodecomponent/node)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
