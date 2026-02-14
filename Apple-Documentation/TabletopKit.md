# TabletopKit Documentation

Source: https://sosumi.ai/documentation/tabletopkit

---
title: TabletopKit
source: https://developer.apple.com/documentation/tabletopkit
timestamp: 2026-02-13T19:02:55.945Z
---

## Essentials

- [Creating tabletop games](/documentation/tabletopkit/creating-tabletop-games)
- [Synchronizing group gameplay with TabletopKit](/documentation/tabletopkit/synchronizing-group-gameplay-with-tabletopkit)
- [TabletopGame](/documentation/tabletopkit/tabletopgame)

### Creating a tabletop game

- [init(tableSetup: TableSetup, version: Int)](/documentation/tabletopkit/tabletopgame/init(tablesetup:version:))
- [var rootPose: Pose3D](/documentation/tabletopkit/tabletopgame/rootpose)
- [func update(deltaTime: Double)](/documentation/tabletopkit/tabletopgame/update(deltatime:))
- [func withCurrentSnapshot((TableSnapshot) -> Void)](/documentation/tabletopkit/tabletopgame/withcurrentsnapshot(_:))

### Adding equipment to the game

- [var equipment: [any Equipment]](/documentation/tabletopkit/tabletopgame/equipment)
- [var equipmentIDs: [EquipmentIdentifier]](/documentation/tabletopkit/tabletopgame/equipmentids)
- [func equipment(matching: EquipmentIdentifier) -> (any Equipment)?](/documentation/tabletopkit/tabletopgame/equipment(matching:))
- [func equipment<E>(of: E.Type) -> [E]](/documentation/tabletopkit/tabletopgame/equipment(of:))
- [func equipment<E>(of: E.Type, forEntity: Entity) -> E?](/documentation/tabletopkit/tabletopgame/equipment(of:forentity:))
- [func equipment<E>(of: E.Type, matching: EquipmentIdentifier) -> E?](/documentation/tabletopkit/tabletopgame/equipment(of:matching:))

### Managing seats

- [func claimAnySeat()](/documentation/tabletopkit/tabletopgame/claimanyseat())
- [func claimSeat(some TableSeat)](/documentation/tabletopkit/tabletopgame/claimseat(_:))
- [func claimSeat(matching: TableSeatIdentifier)](/documentation/tabletopkit/tabletopgame/claimseat(matching:))
- [func releaseSeat()](/documentation/tabletopkit/tabletopgame/releaseseat())

### Getting the player

- [var localPlayer: Player](/documentation/tabletopkit/tabletopgame/localplayer)

### Adding actions

- [func addAction(some TabletopAction)](/documentation/tabletopkit/tabletopgame/addaction(_:)-10j8v)
- [func addAction(some CustomAction)](/documentation/tabletopkit/tabletopgame/addaction(_:)-9zgsy)
- [func addActions(some Sequence<any TabletopAction>)](/documentation/tabletopkit/tabletopgame/addactions(_:))

### Observing actions

- [TabletopGame.Observer](/documentation/tabletopkit/tabletopgame/observer)

#### Handling interaction updates

- [func interactionWasUpdated(TabletopInteraction.Value, snapshot: TableSnapshot)](/documentation/tabletopkit/tabletopgame/observer/interactionwasupdated(_:snapshot:))

#### Validating actions

- [func validateAction(some TabletopAction, snapshot: TableSnapshot) -> Bool](/documentation/tabletopkit/tabletopgame/observer/validateaction(_:snapshot:))
- [func actionIsPending(some TabletopAction, oldSnapshot: TableSnapshot, newSnapshot: TableSnapshot)](/documentation/tabletopkit/tabletopgame/observer/actionispending(_:oldsnapshot:newsnapshot:))
- [func actionWasConfirmed(some TabletopAction, oldSnapshot: TableSnapshot, newSnapshot: TableSnapshot)](/documentation/tabletopkit/tabletopgame/observer/actionwasconfirmed(_:oldsnapshot:newsnapshot:))
- [func actionWasRolledBack(some TabletopAction, snapshot: TableSnapshot)](/documentation/tabletopkit/tabletopgame/observer/actionwasrolledback(_:snapshot:))
- [func actionWasDiscarded(some TabletopAction)](/documentation/tabletopkit/tabletopgame/observer/actionwasdiscarded(_:))

#### Handling seat actions

- [func playerChangedSeats(Player, oldSeat: (any TableSeat)?, newSeat: (any TableSeat)?, snapshot: TableSnapshot)](/documentation/tabletopkit/tabletopgame/observer/playerchangedseats(_:oldseat:newseat:snapshot:))
- [func stateDidResetToBookmark(StateBookmarkIdentifier)](/documentation/tabletopkit/tabletopgame/observer/statedidresettobookmark(_:))

#### Handling cancellations

- [func actionWasCancelled(some TabletopAction, reason: TabletopGame.ActionCancellationReason)](/documentation/tabletopkit/tabletopgame/observer/actionwascancelled(_:reason:))
- [func addObserver(some TabletopGame.Observer)](/documentation/tabletopkit/tabletopgame/addobserver(_:))
- [func removeObserver(some TabletopGame.Observer)](/documentation/tabletopkit/tabletopgame/removeobserver(_:))
- [TabletopGame.ActionCancellationReason](/documentation/tabletopkit/tabletopgame/actioncancellationreason)

#### Cancellation reasons

- [case actionInvalidated](/documentation/tabletopkit/tabletopgame/actioncancellationreason/actioninvalidated)
- [case interactionCancelled](/documentation/tabletopkit/tabletopgame/actioncancellationreason/interactioncancelled)

### Jumping to bookmarks

- [func jumpToBookmark(StateBookmark)](/documentation/tabletopkit/tabletopgame/jumptobookmark(_:))
- [func jumpToBookmark(matching: StateBookmarkIdentifier)](/documentation/tabletopkit/tabletopgame/jumptobookmark(matching:))
- [var bookmarks: [StateBookmarkIdentifier]](/documentation/tabletopkit/tabletopgame/bookmarks)

### Starting interactions

- [func startInteraction(onEquipmentID: EquipmentIdentifier) -> TabletopInteraction.Identifier?](/documentation/tabletopkit/tabletopgame/startinteraction(onequipmentid:))

### Canceling interactions

- [func cancelAllInteractions()](/documentation/tabletopkit/tabletopgame/cancelallinteractions())
- [func cancelInteraction(matching: TabletopInteraction.Identifier)](/documentation/tabletopkit/tabletopgame/cancelinteraction(matching:))

### Rendering the table

- [func addRenderDelegate(some TabletopGame.RenderDelegate)](/documentation/tabletopkit/tabletopgame/addrenderdelegate(_:))
- [func removeRenderDelegate(some TabletopGame.RenderDelegate)](/documentation/tabletopkit/tabletopgame/removerenderdelegate(_:))
- [TabletopGame.RenderDelegate](/documentation/tabletopkit/tabletopgame/renderdelegate)

#### Rendering the game

- [func onUpdate(timeInterval: Double, snapshot: TableSnapshot, visualState: TableVisualState)](/documentation/tabletopkit/tabletopgame/renderdelegate/onupdate(timeinterval:snapshot:visualstate:))
- [func updateRootPose(Pose3D)](/documentation/tabletopkit/tabletopgame/renderdelegate/updaterootpose(_:))
- [EntityRenderDelegate](/documentation/tabletopkit/entityrenderdelegate)

#### Getting the root entity

- [var root: Entity](/documentation/tabletopkit/entityrenderdelegate/root)

#### Rendering the table

- [func updateRootPose(Pose3D)](/documentation/tabletopkit/entityrenderdelegate/updaterootpose(_:))

### Supporting multiple players

- [func attachNetworkCoordinator(some TabletopNetworkSessionCoordinator)](/documentation/tabletopkit/tabletopgame/attachnetworkcoordinator(_:))
- [func detachNetworkCoordinator()](/documentation/tabletopkit/tabletopgame/detachnetworkcoordinator())
- [var multiplayerDelegate: (any TabletopGame.MultiplayerDelegate)?](/documentation/tabletopkit/tabletopgame/multiplayerdelegate-swift.property)
- [TabletopGame.MultiplayerDelegate](/documentation/tabletopkit/tabletopgame/multiplayerdelegate-swift.protocol)

#### Joining games

- [func joinAccepted()](/documentation/tabletopkit/tabletopgame/multiplayerdelegate-swift.protocol/joinaccepted())
- [func playerJoined(PlayerIdentifier)](/documentation/tabletopkit/tabletopgame/multiplayerdelegate-swift.protocol/playerjoined(_:))

#### Handling errors

- [func didRejectPlayer(PlayerIdentifier, reason: any Error)](/documentation/tabletopkit/tabletopgame/multiplayerdelegate-swift.protocol/didrejectplayer(_:reason:))
- [func multiplayerSessionFailed(reason: any Error)](/documentation/tabletopkit/tabletopgame/multiplayerdelegate-swift.protocol/multiplayersessionfailed(reason:))

### Enabling group activities

- [func coordinateWithSession(GroupSession<some GroupActivity>)](/documentation/tabletopkit/tabletopgame/coordinatewithsession(_:))

### Drawing debug representations

- [func debugDraw(options: DebugDrawOptions)](/documentation/tabletopkit/tabletopgame/debugdraw(options:))
- [TableSetup](/documentation/tabletopkit/tablesetup)

### Creating a setup object from a table

- [init(tabletop: some Tabletop)](/documentation/tabletopkit/tablesetup/init(tabletop:)-4cfut)
- [init(tabletop: some EntityTabletop)](/documentation/tabletopkit/tablesetup/init(tabletop:)-7ima6)

### Adding seats to place players

- [func add(seat: some TableSeat)](/documentation/tabletopkit/tablesetup/add(seat:)-a9qw)
- [func add(seat: some EntityTableSeat)](/documentation/tabletopkit/tablesetup/add(seat:)-4alrc)
- [func add(seats: some Sequence)](/documentation/tabletopkit/tablesetup/add(seats:)-4068d)
- [func add(seats: some Sequence)](/documentation/tabletopkit/tablesetup/add(seats:)-4asnu)

### Adding equipment for gameplay

- [func add(equipment: some Equipment)](/documentation/tabletopkit/tablesetup/add(equipment:)-29pef)
- [func add<E>(equipment: E)](/documentation/tabletopkit/tablesetup/add(equipment:)-294gb)
- [func add(equipment: some EntityEquipment)](/documentation/tabletopkit/tablesetup/add(equipment:)-24tv6)
- [func add<E>(equipment: E)](/documentation/tabletopkit/tablesetup/add(equipment:)-7qwj2)
- [func add(equipment: some Sequence)](/documentation/tabletopkit/tablesetup/add(equipment:)-4k6m6)
- [func add<E>(equipment: some Sequence)](/documentation/tabletopkit/tablesetup/add(equipment:)-3d7h9)
- [func add(equipment: some Sequence)](/documentation/tabletopkit/tablesetup/add(equipment:)-9syh2)
- [func add<E>(equipment: some Sequence)](/documentation/tabletopkit/tablesetup/add(equipment:)-9h887)

### Adding counters to keep score

- [func add(counter: ScoreCounter)](/documentation/tabletopkit/tablesetup/add(counter:))
- [func add(counters: some Sequence<ScoreCounter>)](/documentation/tabletopkit/tablesetup/add(counters:))

### Registering an action

- [func register<Action>(action: Action.Type)](/documentation/tabletopkit/tablesetup/register(action:))
- [Tabletop](/documentation/tabletopkit/tabletop)

### Creating a round or rectangular table

- [var shape: TabletopShape](/documentation/tabletopkit/tabletop/shape)

### Displaying the equipment

- [func layoutChildren(for: TableSnapshot, visualState: TableVisualState) -> any EquipmentLayout](/documentation/tabletopkit/tabletop/layoutchildren(for:visualstate:))
- [EntityTabletop](/documentation/tabletopkit/entitytabletop)

### Creating a round or rectangular table

- [var shape: TabletopShape](/documentation/tabletopkit/entitytabletop/shape)

### Displaying the tabletop

- [var entity: Entity](/documentation/tabletopkit/entitytabletop/entity)

### Default Implementations

- [Tabletop Implementations](/documentation/tabletopkit/entitytabletop/tabletop-implementations)

#### Instance Properties

- [var shape: TabletopShape](/documentation/tabletopkit/entitytabletop/shape)
- [TabletopShape](/documentation/tabletopkit/tabletopshape)

### Creating a round or rectangular table

- [static func rectangular(center: Point3D, width: Float, height: Float, thickness: Float, in: UnitLength) -> TabletopShape](/documentation/tabletopkit/tabletopshape/rectangular(center:width:height:thickness:in:))
- [static func round(center: Point3D, radius: Float, thickness: Float, in: UnitLength) -> TabletopShape](/documentation/tabletopkit/tabletopshape/round(center:radius:thickness:in:))

### Creating a table that you render using an entity

- [static func rectangular(entity: Entity) -> TabletopShape](/documentation/tabletopkit/tabletopshape/rectangular(entity:))
- [static func round(entity: Entity) -> TabletopShape](/documentation/tabletopkit/tabletopshape/round(entity:))

## Seats

- [TableState](/documentation/tabletopkit/tablestate)

### Getting the table state

- [var counters: CounterCollection](/documentation/tabletopkit/tablestate/counters)
- [var equipment: EquipmentCollection](/documentation/tabletopkit/tablestate/equipment)
- [var turn: Set<TableSeatIdentifier>](/documentation/tabletopkit/tablestate/turn)
- [TableSeat](/documentation/tabletopkit/tableseat)

### Getting the seat data

- [var initialState: Self.State](/documentation/tabletopkit/tableseat/initialstate)
- [State](/documentation/tabletopkit/tableseat/state)
- [EntityTableSeat](/documentation/tabletopkit/entitytableseat)

### Rendering the equipment

- [var entity: Entity](/documentation/tabletopkit/entitytableseat/entity)
- [TableSeatIdentifier](/documentation/tabletopkit/tableseatidentifier)

### Creating seat identifiers

- [init(Int)](/documentation/tabletopkit/tableseatidentifier/init(_:))

### Getting identifier values

- [let rawValue: Int](/documentation/tabletopkit/tableseatidentifier/rawvalue)
- [TableSeatState](/documentation/tabletopkit/tableseatstate)

### Creating a seat state structure

- [init(pose: TableVisualState.Pose2D, context: UInt64)](/documentation/tabletopkit/tableseatstate/init(pose:context:))

### Setting the data that syncs

- [var playerID: Player.ID?](/documentation/tabletopkit/tableseatstate/playerid)
- [var pose: TableVisualState.Pose2D](/documentation/tabletopkit/tableseatstate/pose)
- [SeatState](/documentation/tabletopkit/seatstate)

### Setting the data that syncs

- [var context: UInt64](/documentation/tabletopkit/seatstate/context)
- [var playerID: PlayerIdentifier?](/documentation/tabletopkit/seatstate/playerid)
- [var pose: TableVisualState.Pose2D](/documentation/tabletopkit/seatstate/pose)

## Equipment

- [Implementing playing card overlap and physical characteristics](/documentation/tabletopkit/implementing-playing-card-overlap-and-physical-characteristics)
- [Equipment](/documentation/tabletopkit/equipment)

### Gettting the initial state of the equipment

- [var initialState: Self.State](/documentation/tabletopkit/equipment/initialstate)
- [State](/documentation/tabletopkit/equipment/state)

### Displaying the equipment

- [func layoutChildren(for: TableSnapshot, visualState: TableVisualState) -> any EquipmentLayout](/documentation/tabletopkit/equipment/layoutchildren(for:visualstate:))
- [func restingOrientation(state: Self.State) -> Rotation3D](/documentation/tabletopkit/equipment/restingorientation(state:))
- [EquipmentCollection](/documentation/tabletopkit/equipmentcollection)

### Getting collection properties

- [var count: Int](/documentation/tabletopkit/equipmentcollection/count)
- [var ids: [EquipmentIdentifier]](/documentation/tabletopkit/equipmentcollection/ids)
- [var state: EquipmentStateCollection](/documentation/tabletopkit/equipmentcollection/state)

### Retrieving equipment identifiers

- [func ids(childrenOf: EquipmentIdentifier) -> [EquipmentIdentifier]](/documentation/tabletopkit/equipmentcollection/ids(childrenof:))
- [func ids(descendantsOf: EquipmentIdentifier) -> [EquipmentIdentifier]](/documentation/tabletopkit/equipmentcollection/ids(descendantsof:))
- [func ids(of: (some Equipment).Type) -> [EquipmentIdentifier]](/documentation/tabletopkit/equipmentcollection/ids(of:))

### Changing the parent

- [func reparent(id: EquipmentIdentifier, to: EquipmentIdentifier)](/documentation/tabletopkit/equipmentcollection/reparent(id:to:))
- [func reparent(ids: [EquipmentIdentifier], to: EquipmentIdentifier)](/documentation/tabletopkit/equipmentcollection/reparent(ids:to:))

### Accessing the subscript

- [subscript<E>(of _: E.Type) -> [(identifier: EquipmentIdentifier, state: E.State)]](/documentation/tabletopkit/equipmentcollection/subscript(of:))
- [EntityEquipment](/documentation/tabletopkit/entityequipment)

### Displaying the equipment

- [var entity: Entity](/documentation/tabletopkit/entityequipment/entity)
- [EquipmentIdentifier](/documentation/tabletopkit/equipmentidentifier)

### Creating equipment identifiers

- [init(Int)](/documentation/tabletopkit/equipmentidentifier/init(_:))

### Getting identifier values

- [let rawValue: Int](/documentation/tabletopkit/equipmentidentifier/rawvalue)
- [EquipmentState](/documentation/tabletopkit/equipmentstate)

### Getting the parent equipment

- [var parentID: EquipmentIdentifier](/documentation/tabletopkit/equipmentstate/parentid)

### Rendering the equipment

- [var boundingBox: Rect3D](/documentation/tabletopkit/equipmentstate/boundingbox)
- [var pose: TableVisualState.Pose2D](/documentation/tabletopkit/equipmentstate/pose)

### Controlling the equipment

- [var seatControl: ControllingSeats](/documentation/tabletopkit/equipmentstate/seatcontrol)
- [var lockedBy: PlayerIdentifier?](/documentation/tabletopkit/equipmentstate/lockedby)
- [EquipmentStateCollection](/documentation/tabletopkit/equipmentstatecollection)

### Accessing the subscript

- [subscript(id _: EquipmentIdentifier) -> (any MutableEquipmentState)?](/documentation/tabletopkit/equipmentstatecollection/subscript(id:))
- [subscript(ids _: some Sequence<EquipmentIdentifier>) -> [(any MutableEquipmentState)?]](/documentation/tabletopkit/equipmentstatecollection/subscript(ids:))
- [subscript<E>(of _: E.Type, id _: EquipmentIdentifier) -> E.State?](/documentation/tabletopkit/equipmentstatecollection/subscript(of:id:))
- [subscript<E>(of _: E.Type, ids _: some Sequence<EquipmentIdentifier>) -> [E.State?]](/documentation/tabletopkit/equipmentstatecollection/subscript(of:ids:))
- [BaseEquipmentState](/documentation/tabletopkit/baseequipmentstate)

### Creating an equipment state

- [init(parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, boundingBox: Rect3D)](/documentation/tabletopkit/baseequipmentstate/init(parentid:seatcontrol:pose:boundingbox:))
- [init(parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, entity: Entity)](/documentation/tabletopkit/baseequipmentstate/init(parentid:seatcontrol:pose:entity:))

### Getting the parent equipment

- [var parentID: EquipmentIdentifier](/documentation/tabletopkit/baseequipmentstate/parentid)

### Rendering the equipment

- [var boundingBox: Rect3D](/documentation/tabletopkit/baseequipmentstate/boundingbox)
- [var pose: TableVisualState.Pose2D](/documentation/tabletopkit/baseequipmentstate/pose)

### Controlling the equipment

- [var lockedBy: PlayerIdentifier?](/documentation/tabletopkit/baseequipmentstate/lockedby)
- [var seatControl: ControllingSeats](/documentation/tabletopkit/baseequipmentstate/seatcontrol)
- [CustomEquipmentState](/documentation/tabletopkit/customequipmentstate)

### Getting the base equipment state

- [var base: BaseEquipmentState](/documentation/tabletopkit/customequipmentstate/base)
- [MutableEquipmentState](/documentation/tabletopkit/mutableequipmentstate)

### Getting the parent

- [var parentID: EquipmentIdentifier](/documentation/tabletopkit/mutableequipmentstate/parentid)

### Rendering the quipment

- [var boundingBox: Rect3D](/documentation/tabletopkit/mutableequipmentstate/boundingbox)
- [var pose: TableVisualState.Pose2D](/documentation/tabletopkit/mutableequipmentstate/pose)

### Controlling the equipment

- [var seatControl: ControllingSeats](/documentation/tabletopkit/mutableequipmentstate/seatcontrol)
- [CardState](/documentation/tabletopkit/cardstate)

### Creating a card state

- [init(faceUp: Bool, parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, boundingBox: Rect3D)](/documentation/tabletopkit/cardstate/init(faceup:parentid:seatcontrol:pose:boundingbox:))
- [init(faceUp: Bool, parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, entity: Entity)](/documentation/tabletopkit/cardstate/init(faceup:parentid:seatcontrol:pose:entity:))
- [static func faceDown(parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, boundingBox: Rect3D) -> CardState](/documentation/tabletopkit/cardstate/facedown(parentid:seatcontrol:pose:boundingbox:))
- [static func faceDown(parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, entity: Entity) -> CardState](/documentation/tabletopkit/cardstate/facedown(parentid:seatcontrol:pose:entity:))
- [static func faceUp(parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, boundingBox: Rect3D) -> CardState](/documentation/tabletopkit/cardstate/faceup(parentid:seatcontrol:pose:boundingbox:))
- [static func faceUp(parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, entity: Entity) -> CardState](/documentation/tabletopkit/cardstate/faceup(parentid:seatcontrol:pose:entity:))

### Getting the card data

- [var faceUp: Bool](/documentation/tabletopkit/cardstate/faceup)

### Getting the parent equipment

- [var parentID: EquipmentIdentifier](/documentation/tabletopkit/cardstate/parentid)

### Rendering the equipment

- [var boundingBox: Rect3D](/documentation/tabletopkit/cardstate/boundingbox)
- [var pose: TableVisualState.Pose2D](/documentation/tabletopkit/cardstate/pose)

### Controlling the equipment

- [var lockedBy: PlayerIdentifier?](/documentation/tabletopkit/cardstate/lockedby)
- [var seatControl: ControllingSeats](/documentation/tabletopkit/cardstate/seatcontrol)
- [DieState](/documentation/tabletopkit/diestate)

### Creating a die state

- [init(value: Int, parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, boundingBox: Rect3D)](/documentation/tabletopkit/diestate/init(value:parentid:seatcontrol:pose:boundingbox:))
- [init(value: Int, parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, entity: Entity)](/documentation/tabletopkit/diestate/init(value:parentid:seatcontrol:pose:entity:))

### Getting the die data

- [var value: Int](/documentation/tabletopkit/diestate/value)

### Getting the parent equipment

- [var parentID: EquipmentIdentifier](/documentation/tabletopkit/diestate/parentid)

### Rendering the equipment

- [var boundingBox: Rect3D](/documentation/tabletopkit/diestate/boundingbox)
- [var pose: TableVisualState.Pose2D](/documentation/tabletopkit/diestate/pose)

### Controlling the equipment

- [var lockedBy: PlayerIdentifier?](/documentation/tabletopkit/diestate/lockedby)
- [var seatControl: ControllingSeats](/documentation/tabletopkit/diestate/seatcontrol)
- [RawValueState](/documentation/tabletopkit/rawvaluestate)

### Creating a die state

- [init(rawValue: UInt64, parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, boundingBox: Rect3D)](/documentation/tabletopkit/rawvaluestate/init(rawvalue:parentid:seatcontrol:pose:boundingbox:))
- [init(rawValue: UInt64, parentID: EquipmentIdentifier, seatControl: ControllingSeats, pose: TableVisualState.Pose2D, entity: Entity)](/documentation/tabletopkit/rawvaluestate/init(rawvalue:parentid:seatcontrol:pose:entity:))

### Getting the die data

- [var rawValue: UInt64](/documentation/tabletopkit/rawvaluestate/rawvalue)

### Getting the parent equipment

- [var parentID: EquipmentIdentifier](/documentation/tabletopkit/rawvaluestate/parentid)

### Rendering the equipment

- [var boundingBox: Rect3D](/documentation/tabletopkit/rawvaluestate/boundingbox)
- [var pose: TableVisualState.Pose2D](/documentation/tabletopkit/rawvaluestate/pose)

### Controlling the equipment

- [var lockedBy: PlayerIdentifier?](/documentation/tabletopkit/rawvaluestate/lockedby)
- [var seatControl: ControllingSeats](/documentation/tabletopkit/rawvaluestate/seatcontrol)
- [ControllingSeats](/documentation/tabletopkit/controllingseats)

### Seats

- [case any](/documentation/tabletopkit/controllingseats/any)
- [case restricted([TableSeatIdentifier])](/documentation/tabletopkit/controllingseats/restricted(_:))
- [case restrictedCurrent([TableSeatIdentifier])](/documentation/tabletopkit/controllingseats/restrictedcurrent(_:))
- [case inherited](/documentation/tabletopkit/controllingseats/inherited)
- [case current](/documentation/tabletopkit/controllingseats/current)

## Equipment layout

- [EquipmentLayout](/documentation/tabletopkit/equipmentlayout)

### Laying out equipment

- [static func planarOverlapping(layout: [EquipmentPose2D], animationDuration: Double?) -> Self](/documentation/tabletopkit/equipmentlayout/planaroverlapping(layout:animationduration:))
- [static func planarStacked(layout: [EquipmentPose2D], animationDuration: Double?) -> Self](/documentation/tabletopkit/equipmentlayout/planarstacked(layout:animationduration:))
- [static func volumetric(layout: [EquipmentPose3D], animationDuration: Double?) -> Self](/documentation/tabletopkit/equipmentlayout/volumetric(layout:animationduration:))
- [DefaultEquipmentLayout](/documentation/tabletopkit/defaultequipmentlayout)
- [EquipmentPose2D](/documentation/tabletopkit/equipmentpose2d)

### Creating an equipment pose object

- [init(id: EquipmentIdentifier, pose: TableVisualState.Pose2D)](/documentation/tabletopkit/equipmentpose2d/init(id:pose:))

### Getting equipment pose properties

- [var id: EquipmentIdentifier](/documentation/tabletopkit/equipmentpose2d/id)
- [var pose: TableVisualState.Pose2D](/documentation/tabletopkit/equipmentpose2d/pose)
- [EquipmentPose3D](/documentation/tabletopkit/equipmentpose3d)

### Creating an equipment pose object

- [init(id: EquipmentIdentifier, pose: Pose3D)](/documentation/tabletopkit/equipmentpose3d/init(id:pose:))

### Getting equipment pose properties

- [var id: EquipmentIdentifier](/documentation/tabletopkit/equipmentpose3d/id)
- [var pose: Pose3D](/documentation/tabletopkit/equipmentpose3d/pose)

## Score counters

- [ScoreCounter](/documentation/tabletopkit/scorecounter)

### Creating score counters

- [init(id: ScoreCounter.ID, value: Int64)](/documentation/tabletopkit/scorecounter/init(id:value:))

### Getting score counter identifiers

- [var id: ScoreCounter.ID](/documentation/tabletopkit/scorecounter/id)
- [ScoreCounter.Identifier](/documentation/tabletopkit/scorecounter/identifier)

#### Creating score counter identifiers

- [init(Int)](/documentation/tabletopkit/scorecounter/identifier/init(_:))

#### Getting the raw value

- [let rawValue: Int](/documentation/tabletopkit/scorecounter/identifier/rawvalue)

### Getting score counter values

- [var value: Int64](/documentation/tabletopkit/scorecounter/value)
- [CounterCollection](/documentation/tabletopkit/countercollection)

### Getting the counter details

- [var count: Int](/documentation/tabletopkit/countercollection/count)
- [var ids: [ScoreCounter.ID]](/documentation/tabletopkit/countercollection/ids)

### Accessing the subscript

- [subscript(ScoreCounter.ID) -> Int64?](/documentation/tabletopkit/countercollection/subscript(_:))

## Players

- [Player](/documentation/tabletopkit/player)

### Identifying players

- [var id: PlayerIdentifier](/documentation/tabletopkit/player/id)
- [PlayerIdentifier](/documentation/tabletopkit/playeridentifier)

### Creating player identifiers

- [init(uuid: UUID)](/documentation/tabletopkit/playeridentifier/init(uuid:))

### Getting identifier values

- [var uuid: UUID](/documentation/tabletopkit/playeridentifier/uuid)

## Actions

- [TabletopAction](/documentation/tabletopkit/tabletopaction)

### Getting the player

- [var playerID: PlayerIdentifier?](/documentation/tabletopkit/tabletopaction/playerid)

### Getting game-specific information

- [var context: UInt64](/documentation/tabletopkit/tabletopaction/context)

### Moving equipment

- [static func moveEquipment(some Equipment, childOf: any Equipment, order: MoveEquipmentAction.Order?, pose: TableVisualState.Pose2D?, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/moveequipment(_:childof:order:pose:context:))
- [static func moveEquipment(matching: EquipmentIdentifier, childOf: EquipmentIdentifier, order: MoveEquipmentAction.Order?, pose: TableVisualState.Pose2D?, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/moveequipment(matching:childof:order:pose:context:))

### Changing equipment state properties

- [static func updateEquipment<E>(E, faceUp: Bool?, seatControl: ControllingSeats?, pose: TableVisualState.Pose2D?, boundingBox: Rect3D?, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/updateequipment(_:faceup:seatcontrol:pose:boundingbox:context:))
- [static func updateEquipment<E>(E, rawValue: UInt64?, seatControl: ControllingSeats?, pose: TableVisualState.Pose2D?, boundingBox: Rect3D?, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/updateequipment(_:rawvalue:seatcontrol:pose:boundingbox:context:))
- [static func updateEquipment<E>(E, seatControl: ControllingSeats?, pose: TableVisualState.Pose2D?, boundingBox: Rect3D?, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/updateequipment(_:seatcontrol:pose:boundingbox:context:))
- [static func updateEquipment<E>(E, state: E.State, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/updateequipment(_:state:context:)-6kawf)
- [static func updateEquipment<E>(E, state: E.State, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/updateequipment(_:state:context:)-88v3m)
- [static func updateEquipment<E>(E, state: E.State, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/updateequipment(_:state:context:)-8tmnn)
- [static func updateEquipment<E>(E, state: E.State, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/updateequipment(_:state:context:)-j62v)
- [static func updateEquipment<E>(E, value: Int?, seatControl: ControllingSeats?, pose: TableVisualState.Pose2D?, boundingBox: Rect3D?, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/updateequipment(_:value:seatcontrol:pose:boundingbox:context:))

### Taking turns

- [static func setTurn(forSeat: some TableSeat, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/setturn(forseat:context:))
- [static func setTurn(forSeats: some Sequence, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/setturn(forseats:context:)-3msxi)
- [static func setTurn(forSeats: some Sequence<any TableSeat>, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/setturn(forseats:context:)-4sgng)
- [static func setTurn(matching: TableSeatIdentifier, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/setturn(matching:context:)-6mq07)
- [static func setTurn(matching: [TableSeatIdentifier], context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/setturn(matching:context:)-88ymv)

### Keeping score

- [static func updateCounter(ScoreCounter, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/updatecounter(_:context:))
- [static func updateCounter(matching: ScoreCounter.Identifier, value: Int64, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/updatecounter(matching:value:context:))

### Creating bookmarks

- [static func createBookmark(StateBookmark, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/createbookmark(_:context:))
- [static func createBookmark(id: StateBookmarkIdentifier, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/createbookmark(id:context:))

### Adding actions

- [static func customAction(some CustomAction, context: UInt64) -> Self](/documentation/tabletopkit/tabletopaction/customaction(_:context:))
- [MoveEquipmentAction](/documentation/tabletopkit/moveequipmentaction)

### Getting the equipment in the action

- [var equipmentID: EquipmentIdentifier](/documentation/tabletopkit/moveequipmentaction/equipmentid)
- [var parentID: EquipmentIdentifier](/documentation/tabletopkit/moveequipmentaction/parentid)
- [var playerID: Player.ID?](/documentation/tabletopkit/moveequipmentaction/playerid)
- [var order: MoveEquipmentAction.Order?](/documentation/tabletopkit/moveequipmentaction/order-swift.property)
- [MoveEquipmentAction.Order](/documentation/tabletopkit/moveequipmentaction/order-swift.enum)

#### Orders

- [case first](/documentation/tabletopkit/moveequipmentaction/order-swift.enum/first)
- [case last](/documentation/tabletopkit/moveequipmentaction/order-swift.enum/last)
- [case before(EquipmentIdentifier)](/documentation/tabletopkit/moveequipmentaction/order-swift.enum/before(_:))
- [case after(EquipmentIdentifier)](/documentation/tabletopkit/moveequipmentaction/order-swift.enum/after(_:))
- [case atIndex(Int)](/documentation/tabletopkit/moveequipmentaction/order-swift.enum/atindex(_:))

### Getting the position of the equipment

- [var pose: TableVisualState.Pose2D?](/documentation/tabletopkit/moveequipmentaction/pose)

### Getting game-specific information

- [var context: UInt64](/documentation/tabletopkit/moveequipmentaction/context)
- [UpdateEquipmentAction](/documentation/tabletopkit/updateequipmentaction)

### Getting the equipment in the action

- [var equipmentID: EquipmentIdentifier](/documentation/tabletopkit/updateequipmentaction/equipmentid)

### Getting the state of the equipment

- [var newState: State?](/documentation/tabletopkit/updateequipmentaction/newstate)

### Getting the context and player identifier

- [var context: UInt64](/documentation/tabletopkit/updateequipmentaction/context)
- [var playerID: Player.ID?](/documentation/tabletopkit/updateequipmentaction/playerid)
- [SetTurnAction](/documentation/tabletopkit/setturnaction)

### Getting the seats involved in a turn

- [var seatIDsInTurn: [TableSeatIdentifier]](/documentation/tabletopkit/setturnaction/seatidsinturn)

### Getting the action properties

- [var context: UInt64](/documentation/tabletopkit/setturnaction/context)
- [var playerID: Player.ID?](/documentation/tabletopkit/setturnaction/playerid)
- [UpdateCounterAction](/documentation/tabletopkit/updatecounteraction)

### Getting counter information

- [var counterID: ScoreCounter.Identifier](/documentation/tabletopkit/updatecounteraction/counterid)
- [var newValue: Int64](/documentation/tabletopkit/updatecounteraction/newvalue)

### Getting game-specific information

- [var context: UInt64](/documentation/tabletopkit/updatecounteraction/context)

### Getting the player identifier

- [var playerID: Player.ID?](/documentation/tabletopkit/updatecounteraction/playerid)
- [CreateBookmarkAction](/documentation/tabletopkit/createbookmarkaction)

### Getting the bookmark

- [var bookmark: StateBookmark](/documentation/tabletopkit/createbookmarkaction/bookmark)

### Getting game-specific information

- [var context: UInt64](/documentation/tabletopkit/createbookmarkaction/context)
- [CustomAction](/documentation/tabletopkit/customaction)

### Creating a custom action

- [init?(from: some TabletopAction)](/documentation/tabletopkit/customaction/init(from:))

### Applying the action

- [func apply(table: inout TableState)](/documentation/tabletopkit/customaction/apply(table:))

### Validating the action

- [func validate(snapshot: TableSnapshot) -> Bool](/documentation/tabletopkit/customaction/validate(snapshot:))

## Interactions

- [Simulating dice rolls as a component for your game](/documentation/tabletopkit/simulating-dice-rolls-as-a-component-for-your-game)
- [TabletopInteraction](/documentation/tabletopkit/tabletopinteraction)

### Performing actions

- [TabletopInteraction.Delegate](/documentation/tabletopkit/tabletopinteraction/delegate)

#### Taking actions

- [func update(interaction: TabletopInteraction)](/documentation/tabletopkit/tabletopinteraction/delegate/update(interaction:))

#### Starting a toss

- [func onTossStart(interaction: TabletopInteraction, outcomes: [TabletopInteraction.TossOutcome])](/documentation/tabletopkit/tabletopinteraction/delegate/ontossstart(interaction:outcomes:))

#### Accepting interactions

- [func shouldAcceptDirectInteraction(initialValue: TabletopInteraction.Value, handoffValue: TabletopInteraction.Value?) -> TabletopInteraction.NewDirectInteractionIntent](/documentation/tabletopkit/tabletopinteraction/delegate/shouldacceptdirectinteraction(initialvalue:handoffvalue:))
- [func shouldAcceptIndirectInteraction(initialValue: TabletopInteraction.Value, handoffValue: TabletopInteraction.Value?) -> TabletopInteraction.NewIndirectInteractionIntent](/documentation/tabletopkit/tabletopinteraction/delegate/shouldacceptindirectinteraction(initialvalue:handoffvalue:))
- [func shouldAcceptInteraction(initialValue: TabletopInteraction.Value, handoffValue: TabletopInteraction.Value?) -> TabletopInteraction.NewInteractionIntent](/documentation/tabletopkit/tabletopinteraction/delegate/shouldacceptinteraction(initialvalue:handoffvalue:))
- [TabletopInteraction.TossOutcome](/documentation/tabletopkit/tabletopinteraction/tossoutcome)

#### Getting the outcome properties

- [var id: EquipmentIdentifier](/documentation/tabletopkit/tabletopinteraction/tossoutcome/id)
- [var pose: TableVisualState.Pose2D](/documentation/tabletopkit/tabletopinteraction/tossoutcome/pose)
- [var restingOrientation: Rotation3D](/documentation/tabletopkit/tabletopinteraction/tossoutcome/restingorientation)
- [var tossableRepresentation: TossableRepresentation](/documentation/tabletopkit/tabletopinteraction/tossoutcome/tossablerepresentation)
- [func addAction(some TabletopAction)](/documentation/tabletopkit/tabletopinteraction/addaction(_:)-1cety)
- [func addAction(some CustomAction)](/documentation/tabletopkit/tabletopinteraction/addaction(_:)-4rx16)
- [func addActions(some Sequence<any TabletopAction>)](/documentation/tabletopkit/tabletopinteraction/addactions(_:))
- [func toss(equipmentID: EquipmentIdentifier, as: TossableRepresentation, linearVelocity: Vector3D?, angularVelocity: Vector3D?)](/documentation/tabletopkit/tabletopinteraction/toss(equipmentid:as:linearvelocity:angularvelocity:))
- [func end()](/documentation/tabletopkit/tabletopinteraction/end())
- [func cancel()](/documentation/tabletopkit/tabletopinteraction/cancel())

### Getting the value of the interaction

- [var value: TabletopInteraction.Value](/documentation/tabletopkit/tabletopinteraction/value-swift.property)
- [TabletopInteraction.Value](/documentation/tabletopkit/tabletopinteraction/value-swift.struct)

#### Getting information about the equipment and game

- [var startingEquipmentID: EquipmentIdentifier](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/startingequipmentid)
- [var controlledEquipmentID: EquipmentIdentifier](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/controlledequipmentid)
- [var allowedDestinations: TabletopInteraction.AllowedDestinations](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/alloweddestinations)

#### Getting the phases

- [var gesturePhase: TabletopInteraction.Value.Phase?](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesturephase)
- [var phase: TabletopInteraction.Value.Phase](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/phase-swift.property)
- [TabletopInteraction.Value.Phase](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/phase-swift.enum)

##### Phases

- [case cancelled](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/phase-swift.enum/cancelled)
- [case ended](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/phase-swift.enum/ended)
- [case started](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/phase-swift.enum/started)
- [case update](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/phase-swift.enum/update)

#### Getting the gestures

- [var gesture: TabletopInteraction.Value.Gesture?](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.property)
- [TabletopInteraction.Value.Gesture](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct)

##### Getting the gesture properties

- [var initialInputDevicePose: Pose3D](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/initialinputdevicepose)
- [var inputDevicePose: Pose3D](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/inputdevicepose)
- [var kind: TabletopInteraction.Value.Gesture.Kind](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/kind-swift.property)
- [TabletopInteraction.Value.Gesture.Kind](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/kind-swift.enum)

###### Gestures

- [case directPinch](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/kind-swift.enum/directpinch)
- [case indirectPinch](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/kind-swift.enum/indirectpinch)
- [var chirality: TabletopInteraction.Value.Gesture.Chirality?](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/chirality-swift.property)
- [TabletopInteraction.Value.Gesture.Chirality](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/chirality-swift.enum)

###### Handedness

- [case left](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/chirality-swift.enum/left)
- [case right](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/chirality-swift.enum/right)
- [var phase: TabletopInteraction.Value.Phase](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/gesture-swift.struct/phase)

#### Getting the proposed locations

- [var proposedDestination: TabletopInteraction.Destination?](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/proposeddestination)
- [var proposedFlip: Bool](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/proposedflip)

#### Getting the position and location

- [var pose: Pose3D](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/pose)
- [var locationOnTable: TableVisualState.Point2D?](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/locationontable)
- [var endLocation: Point3D?](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/endlocation)
- [var endLocationOnTable: TableVisualState.Point2D?](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/endlocationontable)

#### Getting identifiers

- [var id: TabletopInteraction.Value.ID](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/id)
- [var playerID: PlayerIdentifier](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/playerid)

#### Getting the interaction properties

- [var configuration: TabletopInteraction.Configuration](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/configuration)
- [var constants: TabletopInteraction.Constants](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/constants)
- [var initialPose: Pose3D](/documentation/tabletopkit/tabletopinteraction/value-swift.struct/initialpose)

### Setting information about the equipment and pose

- [func setControlledEquipment(matching: EquipmentIdentifier)](/documentation/tabletopkit/tabletopinteraction/setcontrolledequipment(matching:))
- [func setPose(Pose3D)](/documentation/tabletopkit/tabletopinteraction/setpose(_:))

### Managing the interaction destination

- [func setConfiguration(TabletopInteraction.Configuration)](/documentation/tabletopkit/tabletopinteraction/setconfiguration(_:))
- [TabletopInteraction.Configuration](/documentation/tabletopkit/tabletopinteraction/configuration)

#### Creating a configuration

- [init()](/documentation/tabletopkit/tabletopinteraction/configuration/init())
- [init(allowedDestinations: TabletopInteraction.AllowedDestinations)](/documentation/tabletopkit/tabletopinteraction/configuration/init(alloweddestinations:))
- [init(allowedDestinations: TabletopInteraction.AllowedDestinations, hoverAlignment: TabletopInteraction.HoverAlignmentBehavior)](/documentation/tabletopkit/tabletopinteraction/configuration/init(alloweddestinations:hoveralignment:))

#### Getting the allowed destinations

- [var allowedDestinations: TabletopInteraction.AllowedDestinations](/documentation/tabletopkit/tabletopinteraction/configuration/alloweddestinations)

#### Getting the hover alignment

- [var hoverAlignment: TabletopInteraction.HoverAlignmentBehavior](/documentation/tabletopkit/tabletopinteraction/configuration/hoveralignment)
- [TabletopInteraction.AllowedDestinations](/documentation/tabletopkit/tabletopinteraction/alloweddestinations)

#### Destinations

- [case any](/documentation/tabletopkit/tabletopinteraction/alloweddestinations/any)
- [case restricted([EquipmentIdentifier])](/documentation/tabletopkit/tabletopinteraction/alloweddestinations/restricted(_:))
- [TabletopInteraction.Destination](/documentation/tabletopkit/tabletopinteraction/destination)

#### Getting the destination equipment

- [let equipmentID: EquipmentIdentifier](/documentation/tabletopkit/tabletopinteraction/destination/equipmentid)

#### Getting the interaction pose

- [let pose: TableVisualState.Pose2D](/documentation/tabletopkit/tabletopinteraction/destination/pose)
- [func setAllowedDestinations(TabletopInteraction.AllowedDestinations)](/documentation/tabletopkit/tabletopinteraction/setalloweddestinations(_:))

### Getting the interaction identifier

- [TabletopInteraction.Identifier](/documentation/tabletopkit/tabletopinteraction/identifier)

#### Creating an identifier

- [init(Int)](/documentation/tabletopkit/tabletopinteraction/identifier/init(_:))

#### Getting the raw value

- [let rawValue: Int](/documentation/tabletopkit/tabletopinteraction/identifier/rawvalue)

### Determining the dead zone

- [TabletopInteraction.DeadZone](/documentation/tabletopkit/tabletopinteraction/deadzone)

#### Interaction zones

- [case `default`](/documentation/tabletopkit/tabletopinteraction/deadzone/default)
- [case disabled](/documentation/tabletopkit/tabletopinteraction/deadzone/disabled)
- [case within(distance: Double, angle: Angle2D)](/documentation/tabletopkit/tabletopinteraction/deadzone/within(distance:angle:))

### Handling collision behavior

- [TabletopInteraction.Constants](/documentation/tabletopkit/tabletopinteraction/constants)

#### Table interactions

- [case direct(TabletopInteraction.DirectInteractionConstants)](/documentation/tabletopkit/tabletopinteraction/constants/direct(_:))
- [case indirect(TabletopInteraction.IndirectInteractionConstants)](/documentation/tabletopkit/tabletopinteraction/constants/indirect(_:))
- [case programmatic(TabletopInteraction.ProgrammaticInteractionConstants)](/documentation/tabletopkit/tabletopinteraction/constants/programmatic(_:))
- [TabletopInteraction.CollisionTargets](/documentation/tabletopkit/tabletopinteraction/collisiontargets)

#### Getting the table

- [static let table: TabletopInteraction.CollisionTargets](/documentation/tabletopkit/tabletopinteraction/collisiontargets/table)

#### Getting the destination

- [static let proposedDestination: TabletopInteraction.CollisionTargets](/documentation/tabletopkit/tabletopinteraction/collisiontargets/proposeddestination)
- [TabletopInteraction.DirectPickupBehavior](/documentation/tabletopkit/tabletopinteraction/directpickupbehavior)

#### Creating a pickup behavior

- [init(deadZone: TabletopInteraction.DeadZone, collisionResolution: TabletopInteraction.DirectPickupBehavior.CollisionResolutionBehavior)](/documentation/tabletopkit/tabletopinteraction/directpickupbehavior/init(deadzone:collisionresolution:))
- [TabletopInteraction.DirectPickupBehavior.CollisionResolutionBehavior](/documentation/tabletopkit/tabletopinteraction/directpickupbehavior/collisionresolutionbehavior)

##### Resolution behaviors

- [case automatic](/documentation/tabletopkit/tabletopinteraction/directpickupbehavior/collisionresolutionbehavior/automatic)
- [case disabled](/documentation/tabletopkit/tabletopinteraction/directpickupbehavior/collisionresolutionbehavior/disabled)

#### Getting the behavior properties

- [var collisionResolution: TabletopInteraction.DirectPickupBehavior.CollisionResolutionBehavior](/documentation/tabletopkit/tabletopinteraction/directpickupbehavior/collisionresolution)
- [var deadZone: TabletopInteraction.DeadZone](/documentation/tabletopkit/tabletopinteraction/directpickupbehavior/deadzone)
- [static let `default`: TabletopInteraction.DirectPickupBehavior](/documentation/tabletopkit/tabletopinteraction/directpickupbehavior/default)
- [TabletopInteraction.DirectInteractionConstants](/documentation/tabletopkit/tabletopinteraction/directinteractionconstants)

#### Creating a direct interaction

- [init(pickupBehavior: TabletopInteraction.DirectPickupBehavior)](/documentation/tabletopkit/tabletopinteraction/directinteractionconstants/init(pickupbehavior:))

#### Getting the pickup behavior

- [var pickupBehavior: TabletopInteraction.DirectPickupBehavior](/documentation/tabletopkit/tabletopinteraction/directinteractionconstants/pickupbehavior)
- [TabletopInteraction.IndirectRotationAlignmentBehavior](/documentation/tabletopkit/tabletopinteraction/indirectrotationalignmentbehavior)

#### Alignment behaviors

- [case alignToInputDevice](/documentation/tabletopkit/tabletopinteraction/indirectrotationalignmentbehavior/aligntoinputdevice)
- [case alignToInputDeviceAndAutoFlip](/documentation/tabletopkit/tabletopinteraction/indirectrotationalignmentbehavior/aligntoinputdeviceandautoflip)
- [case automatic](/documentation/tabletopkit/tabletopinteraction/indirectrotationalignmentbehavior/automatic)
- [case disabled](/documentation/tabletopkit/tabletopinteraction/indirectrotationalignmentbehavior/disabled)
- [TabletopInteraction.IndirectInteractionConstants](/documentation/tabletopkit/tabletopinteraction/indirectinteractionconstants)

#### Creating an indirect interaction

- [init(rotationAlignment: TabletopInteraction.IndirectRotationAlignmentBehavior)](/documentation/tabletopkit/tabletopinteraction/indirectinteractionconstants/init(rotationalignment:))

#### Getting the rotation alignment

- [var rotationAlignment: TabletopInteraction.IndirectRotationAlignmentBehavior](/documentation/tabletopkit/tabletopinteraction/indirectinteractionconstants/rotationalignment)
- [TabletopInteraction.HoverAlignmentBehavior](/documentation/tabletopkit/tabletopinteraction/hoveralignmentbehavior)

#### Alignment Behaviors

- [case align(TabletopInteraction.HoverAlignmentSource, with: TabletopInteraction.CollisionTargets)](/documentation/tabletopkit/tabletopinteraction/hoveralignmentbehavior/align(_:with:))
- [case automatic(targets: TabletopInteraction.CollisionTargets)](/documentation/tabletopkit/tabletopinteraction/hoveralignmentbehavior/automatic(targets:))
- [case disabled](/documentation/tabletopkit/tabletopinteraction/hoveralignmentbehavior/disabled)
- [case stop(at: TabletopInteraction.CollisionTargets)](/documentation/tabletopkit/tabletopinteraction/hoveralignmentbehavior/stop(at:))
- [TabletopInteraction.HoverAlignmentSource](/documentation/tabletopkit/tabletopinteraction/hoveralignmentsource)

#### Alignment sources

- [case base](/documentation/tabletopkit/tabletopinteraction/hoveralignmentsource/base)
- [case baseOrTop](/documentation/tabletopkit/tabletopinteraction/hoveralignmentsource/baseortop)
- [TabletopInteraction.ProgrammaticInteractionConstants](/documentation/tabletopkit/tabletopinteraction/programmaticinteractionconstants)

### Handling interaction intents

- [TabletopInteraction.NewInteractionIntent](/documentation/tabletopkit/tabletopinteraction/newinteractionintent)

#### Intents

- [case acceptWithConfiguration(TabletopInteraction.Configuration)](/documentation/tabletopkit/tabletopinteraction/newinteractionintent/acceptwithconfiguration(_:))
- [case reject](/documentation/tabletopkit/tabletopinteraction/newinteractionintent/reject)
- [TabletopInteraction.NewDirectInteractionIntent](/documentation/tabletopkit/tabletopinteraction/newdirectinteractionintent)

#### Rejecting the intent

- [static let reject: TabletopInteraction.NewDirectInteractionIntent](/documentation/tabletopkit/tabletopinteraction/newdirectinteractionintent/reject)

#### Accepting the intent

- [static func accept(configuration: TabletopInteraction.Configuration, constants: TabletopInteraction.DirectInteractionConstants) -> TabletopInteraction.NewDirectInteractionIntent](/documentation/tabletopkit/tabletopinteraction/newdirectinteractionintent/accept(configuration:constants:))
- [TabletopInteraction.NewIndirectInteractionIntent](/documentation/tabletopkit/tabletopinteraction/newindirectinteractionintent)

#### Rejecting the intent

- [static let reject: TabletopInteraction.NewIndirectInteractionIntent](/documentation/tabletopkit/tabletopinteraction/newindirectinteractionintent/reject)

#### Accepting the intent

- [static func accept(configuration: TabletopInteraction.Configuration, constants: TabletopInteraction.IndirectInteractionConstants) -> TabletopInteraction.NewIndirectInteractionIntent](/documentation/tabletopkit/tabletopinteraction/newindirectinteractionintent/accept(configuration:constants:))
- [TossableRepresentation](/documentation/tabletopkit/tossablerepresentation)

### Creating geometric shapes

- [static func cube(height: Float, in: UnitLength, restitution: Float?) -> TossableRepresentation](/documentation/tabletopkit/tossablerepresentation/cube(height:in:restitution:))
- [static func decahedron(height: Float, in: UnitLength, restitution: Float?) -> TossableRepresentation](/documentation/tabletopkit/tossablerepresentation/decahedron(height:in:restitution:))
- [static func dodecahedron(height: Float, in: UnitLength, restitution: Float?) -> TossableRepresentation](/documentation/tabletopkit/tossablerepresentation/dodecahedron(height:in:restitution:))
- [static func icosahedron(height: Float, in: UnitLength, restitution: Float?) -> TossableRepresentation](/documentation/tabletopkit/tossablerepresentation/icosahedron(height:in:restitution:))
- [static func octahedron(height: Float, in: UnitLength, restitution: Float?) -> TossableRepresentation](/documentation/tabletopkit/tossablerepresentation/octahedron(height:in:restitution:))
- [static func sphere(radius: Float, in: UnitLength, restitution: Float?) -> TossableRepresentation](/documentation/tabletopkit/tossablerepresentation/sphere(radius:in:restitution:))
- [static func tetrahedron(height: Float, in: UnitLength, restitution: Float?) -> TossableRepresentation](/documentation/tabletopkit/tossablerepresentation/tetrahedron(height:in:restitution:))

### Getting the face

- [func face(for: Rotation3D) -> any TossableRepresentation.TossableFace](/documentation/tabletopkit/tossablerepresentation/face(for:))
- [TossableRepresentation.TossableFace](/documentation/tabletopkit/tossablerepresentation/tossableface)

#### Creating a tossable face

- [init(restingOrientation: Rotation3D)](/documentation/tabletopkit/tossablerepresentation/tossableface/init(restingorientation:))

#### Getting the orientation

- [var restingOrientation: Rotation3D](/documentation/tabletopkit/tossablerepresentation/tossableface/restingorientation)
- [TossableRepresentation.SphereFace](/documentation/tabletopkit/tossablerepresentation/sphereface)

#### Creating a sphere face

- [init(latitude: Angle2D, longitude: Angle2D)](/documentation/tabletopkit/tossablerepresentation/sphereface/init(latitude:longitude:))
- [init(restingOrientation: Rotation3D)](/documentation/tabletopkit/tossablerepresentation/sphereface/init(restingorientation:))

#### Getting the sphere face properties

- [var latitude: Angle2D](/documentation/tabletopkit/tossablerepresentation/sphereface/latitude)
- [var longitude: Angle2D](/documentation/tabletopkit/tossablerepresentation/sphereface/longitude)
- [var restingOrientation: Rotation3D](/documentation/tabletopkit/tossablerepresentation/sphereface/restingorientation)
- [TossableRepresentation.CubeFace](/documentation/tabletopkit/tossablerepresentation/cubeface)

#### Faces

- [case a](/documentation/tabletopkit/tossablerepresentation/cubeface/a)
- [case b](/documentation/tabletopkit/tossablerepresentation/cubeface/b)
- [case c](/documentation/tabletopkit/tossablerepresentation/cubeface/c)
- [case d](/documentation/tabletopkit/tossablerepresentation/cubeface/d)
- [case e](/documentation/tabletopkit/tossablerepresentation/cubeface/e)
- [case f](/documentation/tabletopkit/tossablerepresentation/cubeface/f)

#### Creating a face

- [init(restingOrientation: Rotation3D)](/documentation/tabletopkit/tossablerepresentation/cubeface/init(restingorientation:))

#### Getting the resting orientation

- [var restingOrientation: Rotation3D](/documentation/tabletopkit/tossablerepresentation/cubeface/restingorientation)
- [TossableRepresentation.DecahedronFace](/documentation/tabletopkit/tossablerepresentation/decahedronface)

#### Faces

- [case a](/documentation/tabletopkit/tossablerepresentation/decahedronface/a)
- [case b](/documentation/tabletopkit/tossablerepresentation/decahedronface/b)
- [case c](/documentation/tabletopkit/tossablerepresentation/decahedronface/c)
- [case d](/documentation/tabletopkit/tossablerepresentation/decahedronface/d)
- [case e](/documentation/tabletopkit/tossablerepresentation/decahedronface/e)
- [case f](/documentation/tabletopkit/tossablerepresentation/decahedronface/f)
- [case g](/documentation/tabletopkit/tossablerepresentation/decahedronface/g)
- [case h](/documentation/tabletopkit/tossablerepresentation/decahedronface/h)
- [case i](/documentation/tabletopkit/tossablerepresentation/decahedronface/i)
- [case j](/documentation/tabletopkit/tossablerepresentation/decahedronface/j)

#### Creating a face

- [init(restingOrientation: Rotation3D)](/documentation/tabletopkit/tossablerepresentation/decahedronface/init(restingorientation:))

#### Getting the resting orientation

- [var restingOrientation: Rotation3D](/documentation/tabletopkit/tossablerepresentation/decahedronface/restingorientation)
- [TossableRepresentation.DodecahedronFace](/documentation/tabletopkit/tossablerepresentation/dodecahedronface)

#### Faces

- [case a](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/a)
- [case b](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/b)
- [case c](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/c)
- [case d](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/d)
- [case e](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/e)
- [case f](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/f)
- [case g](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/g)
- [case h](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/h)
- [case i](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/i)
- [case j](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/j)
- [case k](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/k)
- [case l](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/l)

#### Creating a face

- [init(restingOrientation: Rotation3D)](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/init(restingorientation:))

#### Getting the resting orientation

- [var restingOrientation: Rotation3D](/documentation/tabletopkit/tossablerepresentation/dodecahedronface/restingorientation)
- [TossableRepresentation.IcosahedronFace](/documentation/tabletopkit/tossablerepresentation/icosahedronface)

#### Faces

- [case a](/documentation/tabletopkit/tossablerepresentation/icosahedronface/a)
- [case b](/documentation/tabletopkit/tossablerepresentation/icosahedronface/b)
- [case c](/documentation/tabletopkit/tossablerepresentation/icosahedronface/c)
- [case d](/documentation/tabletopkit/tossablerepresentation/icosahedronface/d)
- [case e](/documentation/tabletopkit/tossablerepresentation/icosahedronface/e)
- [case f](/documentation/tabletopkit/tossablerepresentation/icosahedronface/f)
- [case g](/documentation/tabletopkit/tossablerepresentation/icosahedronface/g)
- [case h](/documentation/tabletopkit/tossablerepresentation/icosahedronface/h)
- [case i](/documentation/tabletopkit/tossablerepresentation/icosahedronface/i)
- [case j](/documentation/tabletopkit/tossablerepresentation/icosahedronface/j)
- [case k](/documentation/tabletopkit/tossablerepresentation/icosahedronface/k)
- [case l](/documentation/tabletopkit/tossablerepresentation/icosahedronface/l)
- [case m](/documentation/tabletopkit/tossablerepresentation/icosahedronface/m)
- [case n](/documentation/tabletopkit/tossablerepresentation/icosahedronface/n)
- [case o](/documentation/tabletopkit/tossablerepresentation/icosahedronface/o)
- [case p](/documentation/tabletopkit/tossablerepresentation/icosahedronface/p)
- [case q](/documentation/tabletopkit/tossablerepresentation/icosahedronface/q)
- [case r](/documentation/tabletopkit/tossablerepresentation/icosahedronface/r)
- [case s](/documentation/tabletopkit/tossablerepresentation/icosahedronface/s)
- [case t](/documentation/tabletopkit/tossablerepresentation/icosahedronface/t)

#### Creating a face

- [init(restingOrientation: Rotation3D)](/documentation/tabletopkit/tossablerepresentation/icosahedronface/init(restingorientation:))

#### Getting the resting orientation

- [var restingOrientation: Rotation3D](/documentation/tabletopkit/tossablerepresentation/icosahedronface/restingorientation)
- [TossableRepresentation.OctahedronFace](/documentation/tabletopkit/tossablerepresentation/octahedronface)

#### Faces

- [case a](/documentation/tabletopkit/tossablerepresentation/octahedronface/a)
- [case b](/documentation/tabletopkit/tossablerepresentation/octahedronface/b)
- [case c](/documentation/tabletopkit/tossablerepresentation/octahedronface/c)
- [case d](/documentation/tabletopkit/tossablerepresentation/octahedronface/d)
- [case e](/documentation/tabletopkit/tossablerepresentation/octahedronface/e)
- [case f](/documentation/tabletopkit/tossablerepresentation/octahedronface/f)
- [case g](/documentation/tabletopkit/tossablerepresentation/octahedronface/g)
- [case h](/documentation/tabletopkit/tossablerepresentation/octahedronface/h)

#### Creating a face

- [init(restingOrientation: Rotation3D)](/documentation/tabletopkit/tossablerepresentation/octahedronface/init(restingorientation:))

#### Getting the resting orientation

- [var restingOrientation: Rotation3D](/documentation/tabletopkit/tossablerepresentation/octahedronface/restingorientation)
- [TossableRepresentation.TetrahedronFace](/documentation/tabletopkit/tossablerepresentation/tetrahedronface)

#### Faces

- [case a](/documentation/tabletopkit/tossablerepresentation/tetrahedronface/a)
- [case b](/documentation/tabletopkit/tossablerepresentation/tetrahedronface/b)
- [case c](/documentation/tabletopkit/tossablerepresentation/tetrahedronface/c)
- [case d](/documentation/tabletopkit/tossablerepresentation/tetrahedronface/d)

#### Creating a face

- [init(restingOrientation: Rotation3D)](/documentation/tabletopkit/tossablerepresentation/tetrahedronface/init(restingorientation:))

#### Getting the resting orientation

- [var restingOrientation: Rotation3D](/documentation/tabletopkit/tossablerepresentation/tetrahedronface/restingorientation)
- [TableSnapshot](/documentation/tabletopkit/tablesnapshot)

### Getting the table entity

- [var tableEntity: Entity?](/documentation/tabletopkit/tablesnapshot/tableentity)

### Getting information on seats

- [var turn: Set<TableSeatIdentifier>](/documentation/tabletopkit/tablesnapshot/turn)
- [var seats: [any TableSeat]](/documentation/tabletopkit/tablesnapshot/seats)
- [var seatIDs: [TableSeatIdentifier]](/documentation/tabletopkit/tablesnapshot/seatids)
- [func seat<S>(of: S.Type, for: Player) -> (S, S.State)?](/documentation/tabletopkit/tablesnapshot/seat(of:for:))
- [func seat<S>(of: S.Type, matching: TableSeatIdentifier) -> (S, S.State)?](/documentation/tabletopkit/tablesnapshot/seat(of:matching:))
- [func seats<S>(of: S.Type) -> [(S, S.State)]](/documentation/tabletopkit/tablesnapshot/seats(of:))
- [func state<E>(for: E) -> E.State](/documentation/tabletopkit/tablesnapshot/state(for:))
- [func state(matching: TableSeatIdentifier) -> (any SeatState)?](/documentation/tabletopkit/tablesnapshot/state(matching:)-ear2)
- [func entity(forSeat: some EntityTableSeat) -> Entity?](/documentation/tabletopkit/tablesnapshot/entity(forseat:))
- [func entity(matching: TableSeatIdentifier) -> Entity?](/documentation/tabletopkit/tablesnapshot/entity(matching:)-7ps7s)

### Getting cursors

- [var cursors: [TableCursor]](/documentation/tabletopkit/tablesnapshot/cursors)
- [func cursor(matching: TableCursorIdentifier) -> TableCursor?](/documentation/tabletopkit/tablesnapshot/cursor(matching:))
- [func cursor(controlling: EquipmentIdentifier) -> TableCursor?](/documentation/tabletopkit/tablesnapshot/cursor(controlling:))
- [func cursors(forPlayer: Player) -> [TableCursor]](/documentation/tabletopkit/tablesnapshot/cursors(forplayer:))
- [func cursors(hovering: EquipmentIdentifier) -> [TableCursor]](/documentation/tabletopkit/tablesnapshot/cursors(hovering:))
- [func cursors(controlling: some Sequence<EquipmentIdentifier>) -> [TableCursor]](/documentation/tabletopkit/tablesnapshot/cursors(controlling:))
- [func cursors(for: Player) -> [TableCursor]](/documentation/tabletopkit/tablesnapshot/cursors(for:))
- [func cursors(matching: TabletopInteraction.Identifier) -> [TableCursor]](/documentation/tabletopkit/tablesnapshot/cursors(matching:))

### Getting information on equipment

- [func equipment<E>(of: E.Type) -> [(E, E.State)]](/documentation/tabletopkit/tablesnapshot/equipment(of:))
- [func equipment<E>(of: E.Type, childrenOf: some Equipment) -> [(E, E.State)]](/documentation/tabletopkit/tablesnapshot/equipment(of:childrenof:)-4z4s1)
- [func equipment<E>(of: E.Type, childrenOf: EquipmentIdentifier) -> [(E, E.State)]](/documentation/tabletopkit/tablesnapshot/equipment(of:childrenof:)-5w137)
- [func equipment<E>(of: E.Type, matching: some Sequence<EquipmentIdentifier>) -> [(E, E.State)]](/documentation/tabletopkit/tablesnapshot/equipment(of:matching:)-7ai0c)
- [func equipment<E>(of: E.Type, matching: EquipmentIdentifier) -> (E, E.State)?](/documentation/tabletopkit/tablesnapshot/equipment(of:matching:)-8qve2)
- [func equipmentIDs() -> [EquipmentIdentifier]](/documentation/tabletopkit/tablesnapshot/equipmentids())
- [func equipmentIDs(childrenOf: some Equipment) -> [EquipmentIdentifier]](/documentation/tabletopkit/tablesnapshot/equipmentids(childrenof:)-432sk)
- [func equipmentIDs(childrenOf: EquipmentIdentifier) -> [EquipmentIdentifier]](/documentation/tabletopkit/tablesnapshot/equipmentids(childrenof:)-f1sp)
- [func state(matching: EquipmentIdentifier) -> (any EquipmentState)?](/documentation/tabletopkit/tablesnapshot/state(matching:)-u35k)
- [func entity(matching: EquipmentIdentifier) -> Entity?](/documentation/tabletopkit/tablesnapshot/entity(matching:)-vb9w)
- [func entity(forEquipment: some EntityEquipment) -> Entity?](/documentation/tabletopkit/tablesnapshot/entity(forequipment:))

### Getting score counters

- [var counters: [ScoreCounter]](/documentation/tabletopkit/tablesnapshot/counters)
- [func counter(matching: ScoreCounter.ID) -> ScoreCounter?](/documentation/tabletopkit/tablesnapshot/counter(matching:))
- [TableVisualState](/documentation/tabletopkit/tablevisualstate)

### Representing collision states

- [var contacts: some Sequence<TableVisualState.Contact>](/documentation/tabletopkit/tablevisualstate/contacts)
- [func contacts<E>(of: E.Type) -> some Sequence<TableVisualState.Contact>
](/documentation/tabletopkit/tablevisualstate/contacts(of:))
- [TableVisualState.Contact](/documentation/tabletopkit/tablevisualstate/contact)

#### Getting collision objects

- [let collider: any Equipment](/documentation/tabletopkit/tablevisualstate/contact/collider)
- [let collidedWithEquipment: EquipmentIdentifier?](/documentation/tabletopkit/tablevisualstate/contact/collidedwithequipment)

#### Getting collision metrics

- [let impulse: Float](/documentation/tabletopkit/tablevisualstate/contact/impulse)
- [let normal: Vector3D](/documentation/tabletopkit/tablevisualstate/contact/normal)
- [let position: Point3D](/documentation/tabletopkit/tablevisualstate/contact/position)

### Representing 2D states

- [TableVisualState.Point2D](/documentation/tabletopkit/tablevisualstate/point2d)

#### Creating 2D point states

- [init()](/documentation/tabletopkit/tablevisualstate/point2d/init())
- [init(projecting: Point3D)](/documentation/tabletopkit/tablevisualstate/point2d/init(projecting:))
- [init(x: Double, z: Double)](/documentation/tabletopkit/tablevisualstate/point2d/init(x:z:))

#### Getting 2D point properties

- [var x: Double](/documentation/tabletopkit/tablevisualstate/point2d/x)
- [var z: Double](/documentation/tabletopkit/tablevisualstate/point2d/z)
- [static let zero: TableVisualState.Point2D](/documentation/tabletopkit/tablevisualstate/point2d/zero)

#### Default Implementations

- [Decodable Implementations](/documentation/tabletopkit/tablevisualstate/point2d/decodable-implementations)

##### Initializers

- [init(from: any Decoder) throws](/documentation/tabletopkit/tablevisualstate/point2d/init(from:))
- [Encodable Implementations](/documentation/tabletopkit/tablevisualstate/point2d/encodable-implementations)

##### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/tabletopkit/tablevisualstate/point2d/encode(to:))
- [TableVisualState.Pose2D](/documentation/tabletopkit/tablevisualstate/pose2d)

#### Creating 2D pose objects

- [init()](/documentation/tabletopkit/tablevisualstate/pose2d/init())
- [init(position: TableVisualState.Point2D, rotation: Angle2D)](/documentation/tabletopkit/tablevisualstate/pose2d/init(position:rotation:))
- [init(projecting: Pose3D)](/documentation/tabletopkit/tablevisualstate/pose2d/init(projecting:))

#### Getting 2D pose properties

- [var position: TableVisualState.Point2D](/documentation/tabletopkit/tablevisualstate/pose2d/position)
- [var rotation: Angle2D](/documentation/tabletopkit/tablevisualstate/pose2d/rotation)

#### Getting the identifier

- [static var identity: TableVisualState.Pose2D](/documentation/tabletopkit/tablevisualstate/pose2d/identity)

#### Default Implementations

- [Decodable Implementations](/documentation/tabletopkit/tablevisualstate/pose2d/decodable-implementations)

##### Initializers

- [init(from: any Decoder) throws](/documentation/tabletopkit/tablevisualstate/pose2d/init(from:))
- [Encodable Implementations](/documentation/tabletopkit/tablevisualstate/pose2d/encodable-implementations)

##### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/tabletopkit/tablevisualstate/pose2d/encode(to:))

### Representing 3D states

- [TableVisualState.OrientedRect3D](/documentation/tabletopkit/tablevisualstate/orientedrect3d)

#### Creating 3D rectangle states

- [init()](/documentation/tabletopkit/tablevisualstate/orientedrect3d/init())
- [init(pose: Pose3D, size: Size3D)](/documentation/tabletopkit/tablevisualstate/orientedrect3d/init(pose:size:))
- [init(rotation: Rotation3D, rect: Rect3D)](/documentation/tabletopkit/tablevisualstate/orientedrect3d/init(rotation:rect:))

#### Getting 3D rectangle properties

- [var pose: Pose3D](/documentation/tabletopkit/tablevisualstate/orientedrect3d/pose)
- [var size: Size3D](/documentation/tabletopkit/tablevisualstate/orientedrect3d/size)

#### Default Implementations

- [Decodable Implementations](/documentation/tabletopkit/tablevisualstate/orientedrect3d/decodable-implementations)

##### Initializers

- [init(from: any Decoder) throws](/documentation/tabletopkit/tablevisualstate/orientedrect3d/init(from:))
- [Encodable Implementations](/documentation/tabletopkit/tablevisualstate/orientedrect3d/encodable-implementations)

##### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/tabletopkit/tablevisualstate/orientedrect3d/encode(to:))
- [func bounds(for: some Equipment) -> TableVisualState.OrientedRect3D?](/documentation/tabletopkit/tablevisualstate/bounds(for:))
- [func bounds(forEquipment: some Equipment) -> TableVisualState.OrientedRect3D?](/documentation/tabletopkit/tablevisualstate/bounds(forequipment:))
- [func bounds(matching: EquipmentIdentifier) -> TableVisualState.OrientedRect3D?](/documentation/tabletopkit/tablevisualstate/bounds(matching:))
- [func goalBounds(forEquipment: some Equipment) -> TableVisualState.OrientedRect3D?](/documentation/tabletopkit/tablevisualstate/goalbounds(forequipment:))
- [func goalBounds(matching: EquipmentIdentifier) -> TableVisualState.OrientedRect3D?](/documentation/tabletopkit/tablevisualstate/goalbounds(matching:))
- [var tableBounds: TableVisualState.OrientedRect3D?](/documentation/tabletopkit/tablevisualstate/tablebounds)

### Representing seat states

- [func pose(for: some Equipment) -> Pose3D?](/documentation/tabletopkit/tablevisualstate/pose(for:)-50h4r)
- [func pose(for: some TableSeat) -> Pose3D?](/documentation/tabletopkit/tablevisualstate/pose(for:)-8pm0h)
- [func pose(forSeat: some TableSeat) -> Pose3D?](/documentation/tabletopkit/tablevisualstate/pose(forseat:))
- [func pose(matching: TableSeatIdentifier) -> Pose3D?](/documentation/tabletopkit/tablevisualstate/pose(matching:)-6bo29)
- [func pose(matching: EquipmentIdentifier) -> Pose3D?](/documentation/tabletopkit/tablevisualstate/pose(matching:)-8nqm2)

### Representing the goal

- [func goalBounds(for: some Equipment) -> TableVisualState.OrientedRect3D?](/documentation/tabletopkit/tablevisualstate/goalbounds(for:))
- [func goalPose(for: some Equipment) -> Pose3D?](/documentation/tabletopkit/tablevisualstate/goalpose(for:))
- [func goalPose(matching: EquipmentIdentifier) -> Pose3D?](/documentation/tabletopkit/tablevisualstate/goalpose(matching:))
- [TableCursor](/documentation/tabletopkit/tablecursor)

### Getting the associated interaction

- [var interactionID: TabletopInteraction.Identifier](/documentation/tabletopkit/tablecursor/interactionid)

### Getting the player performing the interaction

- [var playerID: PlayerIdentifier](/documentation/tabletopkit/tablecursor/playerid)

### Getting information about the equipment in the interaction

- [let controlledEquipmentPose: EquipmentPose3D](/documentation/tabletopkit/tablecursor/controlledequipmentpose)
- [var hovering: TabletopInteraction.Destination?](/documentation/tabletopkit/tablecursor/hovering)

### Getting the cursor identifier

- [var id: TableCursor.ID](/documentation/tabletopkit/tablecursor/id)
- [TableCursorIdentifier](/documentation/tabletopkit/tablecursoridentifier)

### Creating cursor identifiers

- [init(Int)](/documentation/tabletopkit/tablecursoridentifier/init(_:))

### Getting identifier values

- [let rawValue: Int](/documentation/tabletopkit/tablecursoridentifier/rawvalue)

## Bookmarks

- [StateBookmark](/documentation/tabletopkit/statebookmark)

### Initializing bookmarks

- [init(id: StateBookmark.ID)](/documentation/tabletopkit/statebookmark/init(id:))
- [StateBookmarkIdentifier](/documentation/tabletopkit/statebookmarkidentifier)

### Creating bookmark identifiers

- [init(Int)](/documentation/tabletopkit/statebookmarkidentifier/init(_:))

### Getting identifier values

- [let rawValue: Int](/documentation/tabletopkit/statebookmarkidentifier/rawvalue)

## Multiplayer network session

- [TabletopNetworkSession](/documentation/tabletopkit/tabletopnetworksession)

### Joining multiplayer games

- [func start()](/documentation/tabletopkit/tabletopnetworksession/start())
- [func join()](/documentation/tabletopkit/tabletopnetworksession/join())
- [func leave()](/documentation/tabletopkit/tabletopnetworksession/leave())
- [func terminate()](/documentation/tabletopkit/tabletopnetworksession/terminate())

### Changing the arbiter role between players

- [func becomeArbiter()](/documentation/tabletopkit/tabletopnetworksession/becomearbiter())
- [func followArbiter(TabletopNetworkSession<Coordinator>.Peer)](/documentation/tabletopkit/tabletopnetworksession/followarbiter(_:))

### Managing network session peers

- [var peers: Set<TabletopNetworkSession<Coordinator>.Peer>](/documentation/tabletopkit/tabletopnetworksession/peers)
- [func addPeer(TabletopNetworkSession<Coordinator>.Peer)](/documentation/tabletopkit/tabletopnetworksession/addpeer(_:))
- [func removePeer(TabletopNetworkSession<Coordinator>.Peer)](/documentation/tabletopkit/tabletopnetworksession/removepeer(_:))
- [TabletopNetworkSession.Peer](/documentation/tabletopkit/tabletopnetworksession/peer)

### Receiving messages from peers

- [func processIncomingMessage(Data, from: TabletopNetworkSession<Coordinator>.Peer)](/documentation/tabletopkit/tabletopnetworksession/processincomingmessage(_:from:))
- [func processIncomingUnreliableMessage(Data, from: TabletopNetworkSession<Coordinator>.Peer)](/documentation/tabletopkit/tabletopnetworksession/processincomingunreliablemessage(_:from:))
- [TabletopNetworkSessionCoordinator](/documentation/tabletopkit/tabletopnetworksessioncoordinator)

### Starting network sessions

- [func coordinateWithSession(Self.NetworkSession)](/documentation/tabletopkit/tabletopnetworksessioncoordinator/coordinatewithsession(_:))
- [TabletopNetworkSessionCoordinator.NetworkSession](/documentation/tabletopkit/tabletopnetworksessioncoordinator/networksession)

### Managing network session peers

- [func peerJoinedGame(Self.Peer.ID)](/documentation/tabletopkit/tabletopnetworksessioncoordinator/peerjoinedgame(_:))
- [func peerLeftGame(Self.Peer.ID)](/documentation/tabletopkit/tabletopnetworksessioncoordinator/peerleftgame(_:))
- [Peer](/documentation/tabletopkit/tabletopnetworksessioncoordinator/peer)

### Sending messages between peers

- [func sendMessage(Data, to: Set<Self.Peer>, completion: (TabletopSendMessageResult) -> Void)](/documentation/tabletopkit/tabletopnetworksessioncoordinator/sendmessage(_:to:completion:))
- [func sendMessageUnreliably(Data, to: Set<Self.Peer>, completion: (TabletopSendMessageResult) -> Void)](/documentation/tabletopkit/tabletopnetworksessioncoordinator/sendmessageunreliably(_:to:completion:))
- [TabletopSendMessageResult](/documentation/tabletopkit/tabletopsendmessageresult)

### Message results

- [case success](/documentation/tabletopkit/tabletopsendmessageresult/success)
- [case failure](/documentation/tabletopkit/tabletopsendmessageresult/failure)

## Debugging

- [DebugDrawOptions](/documentation/tabletopkit/debugdrawoptions)

### Setting the types of items

- [static let drawEquipment: DebugDrawOptions](/documentation/tabletopkit/debugdrawoptions/drawequipment)
- [static let drawSeats: DebugDrawOptions](/documentation/tabletopkit/debugdrawoptions/drawseats)
- [static let drawTable: DebugDrawOptions](/documentation/tabletopkit/debugdrawoptions/drawtable)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
