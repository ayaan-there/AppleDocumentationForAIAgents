# GameKit Documentation

Source: https://sosumi.ai/documentation/gamekit

---
title: GameKit
source: https://developer.apple.com/documentation/gamekit
timestamp: 2026-02-13T19:23:22.516Z
---

## Essentials

- [Initializing and configuring Game Center](/documentation/gamekit/initializing-and-configuring-game-center)
- [Authenticating a player](/documentation/gamekit/authenticating-a-player)
- [Improving the player experience for games with large downloads](/documentation/gamekit/improving-the-player-experience-for-games-with-large-downloads)
- [Game Center Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.game-center)

## Players

- [Connecting players with their friends in your game](/documentation/gamekit/connecting-players-with-their-friends-in-your-game)
- [Saving the player’s game data to an iCloud account](/documentation/gamekit/saving-the-player-s-game-data-to-an-icloud-account)
- [Protecting the player’s privacy using scoped identifiers](/documentation/gamekit/protecting-the-player-s-privacy-using-scoped-identifiers)
- [GKLocalPlayer](/documentation/gamekit/gklocalplayer)

### Accessing the Local Player

- [class var local: GKLocalPlayer](/documentation/gamekit/gklocalplayer/local-oaa8)

### Authenticating the Local Player

- [var authenticateHandler: ((UIViewController?, (any Error)?) -> Void)?](/documentation/gamekit/gklocalplayer/authenticatehandler)
- [var isAuthenticated: Bool](/documentation/gamekit/gklocalplayer/isauthenticated)
- [func fetchItems(forIdentityVerificationSignature: ((URL?, Data?, Data?, UInt64, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/fetchitems(foridentityverificationsignature:))
- [static let GKPlayerAuthenticationDidChangeNotificationName: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gkplayerauthenticationdidchangenotificationname)

### Determining Whether the Player Is Underage or Restricted

- [var isUnderage: Bool](/documentation/gamekit/gklocalplayer/isunderage)
- [var isMultiplayerGamingRestricted: Bool](/documentation/gamekit/gklocalplayer/ismultiplayergamingrestricted)
- [var isPersonalizedCommunicationRestricted: Bool](/documentation/gamekit/gklocalplayer/ispersonalizedcommunicationrestricted)

### Accessing Friends and Recents

- [func loadFriendsAuthorizationStatus((GKFriendsAuthorizationStatus, (any Error)?) -> Void)](/documentation/gamekit/gklocalplayer/loadfriendsauthorizationstatus(_:))
- [GKFriendsAuthorizationStatus](/documentation/gamekit/gkfriendsauthorizationstatus)

#### Authorization Statuses

- [case authorized](/documentation/gamekit/gkfriendsauthorizationstatus/authorized)
- [case denied](/documentation/gamekit/gkfriendsauthorizationstatus/denied)
- [case notDetermined](/documentation/gamekit/gkfriendsauthorizationstatus/notdetermined)
- [case restricted](/documentation/gamekit/gkfriendsauthorizationstatus/restricted)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkfriendsauthorizationstatus/init(rawvalue:))
- [func loadFriends(([GKPlayer]?, (any Error)?) -> Void)](/documentation/gamekit/gklocalplayer/loadfriends(_:))
- [func loadFriends(identifiedBy: [String], completionHandler: ([GKPlayer]?, (any Error)?) -> Void)](/documentation/gamekit/gklocalplayer/loadfriends(identifiedby:completionhandler:))
- [NSGKFriendListUsageDescription](/documentation/bundleresources/information-property-list/nsgkfriendlistusagedescription)
- [func loadChallengableFriends(completionHandler: (([GKPlayer]?, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/loadchallengablefriends(completionhandler:))
- [func loadRecentPlayers(completionHandler: (([GKPlayer]?, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/loadrecentplayers(completionhandler:))

### Adding Friends

- [var isPresentingFriendRequestViewController: Bool](/documentation/gamekit/gklocalplayer/ispresentingfriendrequestviewcontroller)
- [func presentFriendRequestCreator(from: UIViewController) throws](/documentation/gamekit/gklocalplayer/presentfriendrequestcreator(from:)-7j1kn)
- [func presentFriendRequestCreator(from: NSWindow?) throws](/documentation/gamekit/gklocalplayer/presentfriendrequestcreator(from:)-7clh6)

### Working with Leaderboards

- [func loadDefaultLeaderboardIdentifier(completionHandler: ((String?, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/loaddefaultleaderboardidentifier(completionhandler:))
- [func setDefaultLeaderboardIdentifier(String, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/setdefaultleaderboardidentifier(_:completionhandler:))

### Registering Listeners

- [func register(any GKLocalPlayerListener)](/documentation/gamekit/gklocalplayer/register(_:))
- [func unregisterAllListeners()](/documentation/gamekit/gklocalplayer/unregisteralllisteners())
- [func unregisterListener(any GKLocalPlayerListener)](/documentation/gamekit/gklocalplayer/unregisterlistener(_:))

### Saving Game Data

- [Saving the player’s game data to an iCloud account](/documentation/gamekit/saving-the-player-s-game-data-to-an-icloud-account)
- [func saveGameData(Data, withName: String, completionHandler: ((GKSavedGame?, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/savegamedata(_:withname:completionhandler:))
- [func fetchSavedGames(completionHandler: (([GKSavedGame]?, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/fetchsavedgames(completionhandler:))
- [func resolveConflictingSavedGames([GKSavedGame], with: Data, completionHandler: (([GKSavedGame]?, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/resolveconflictingsavedgames(_:with:completionhandler:))
- [func deleteSavedGames(withName: String, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/deletesavedgames(withname:completionhandler:))
- [GKSavedGame](/documentation/gamekit/gksavedgame)

#### Loading Saved Game Data

- [func loadData(completionHandler: ((Data?, (any Error)?) -> Void)?)](/documentation/gamekit/gksavedgame/loaddata(completionhandler:))

#### Retrieving Information About a Saved Game File

- [var name: String?](/documentation/gamekit/gksavedgame/name)
- [var modificationDate: Date?](/documentation/gamekit/gksavedgame/modificationdate)
- [var deviceName: String?](/documentation/gamekit/gksavedgame/devicename)
- [GKSavedGameListener](/documentation/gamekit/gksavedgamelistener)

#### Handling Saved Game Conflicts

- [func player(GKPlayer, hasConflictingSavedGames: [GKSavedGame])](/documentation/gamekit/gksavedgamelistener/player(_:hasconflictingsavedgames:))

#### Handling Saved Game Changes

- [func player(GKPlayer, didModifySavedGame: GKSavedGame)](/documentation/gamekit/gksavedgamelistener/player(_:didmodifysavedgame:))

### Deprecated

- [Deprecated symbols](/documentation/gamekit/gklocalplayer-deprecated-symbols)

#### Deprecated properties

- [var friends: [String]?](/documentation/gamekit/gklocalplayer/friends)

#### Deprecated methods

- [func authenticate(completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/authenticate(completionhandler:))
- [func generateIdentityVerificationSignature(completionHandler: ((URL?, Data?, Data?, UInt64, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/generateidentityverificationsignature(completionhandler:))
- [func loadDefaultLeaderboardCategoryID(completionHandler: ((String?, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/loaddefaultleaderboardcategoryid(completionhandler:))
- [func loadFriendPlayers(completionHandler: (([GKPlayer]?, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/loadfriendplayers(completionhandler:))
- [func loadFriendsObsoleted(completionHandler: (([String]?, (any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/loadfriendsobsoleted(completionhandler:))
- [func setDefaultLeaderboardCategoryID(String?, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gklocalplayer/setdefaultleaderboardcategoryid(_:completionhandler:))
- [GKPlayer](/documentation/gamekit/gkplayer)

### Identifying the player

- [var gamePlayerID: String](/documentation/gamekit/gkplayer/gameplayerid)
- [var teamPlayerID: String](/documentation/gamekit/gkplayer/teamplayerid)
- [func scopedIDsArePersistent() -> Bool](/documentation/gamekit/gkplayer/scopedidsarepersistent())
- [let GKPlayerIDNoLongerAvailable: String](/documentation/gamekit/gkplayeridnolongeravailable)
- [var playerID: String](/documentation/gamekit/gkplayer/playerid)

### Accessing player details

- [var alias: String](/documentation/gamekit/gkplayer/alias)
- [var displayName: String](/documentation/gamekit/gkplayer/displayname)
- [var isInvitable: Bool](/documentation/gamekit/gkplayer/isinvitable)
- [var isFriend: Bool](/documentation/gamekit/gkplayer/isfriend)

### Loading player photos

- [func loadPhoto(for: GKPlayer.PhotoSize, withCompletionHandler: ((UIImage?, (any Error)?) -> Void)?)](/documentation/gamekit/gkplayer/loadphoto(for:withcompletionhandler:))
- [GKPlayer.PhotoSize](/documentation/gamekit/gkplayer/photosize)

#### Constants

- [case small](/documentation/gamekit/gkplayer/photosize/small)
- [case normal](/documentation/gamekit/gkplayer/photosize/normal)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkplayer/photosize/init(rawvalue:))

### Creating a guest player

- [class func anonymousGuestPlayer(withIdentifier: String) -> Self](/documentation/gamekit/gkplayer/anonymousguestplayer(withidentifier:))
- [var guestIdentifier: String?](/documentation/gamekit/gkplayer/guestidentifier)

### Observing notifications

- [static let GKPlayerDidChangeNotificationName: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gkplayerdidchangenotificationname)

### Loading player details

- [class func loadPlayers(forIdentifiers: [String], withCompletionHandler: (([GKPlayer]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkplayer/loadplayers(foridentifiers:withcompletionhandler:))
- [GKBasePlayer](/documentation/gamekit/gkbaseplayer)

### Identifying a Player

- [var displayName: String?](/documentation/gamekit/gkbaseplayer/displayname)
- [var playerID: String?](/documentation/gamekit/gkbaseplayer/playerid)
- [GKLocalPlayerListener](/documentation/gamekit/gklocalplayerlistener)
- [static let GKPlayerAuthenticationDidChangeNotificationName: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gkplayerauthenticationdidchangenotificationname)
- [static let GKPlayerDidChangeNotificationName: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gkplayerdidchangenotificationname)

## Game Center interfaces

- [Adding an access point to your game](/documentation/gamekit/adding-an-access-point-to-your-game)
- [Displaying the Game Center dashboard](/documentation/gamekit/displaying-the-game-center-dashboard)
- [GKAccessPoint](/documentation/gamekit/gkaccesspoint)

### Getting the shared access point

- [class var shared: GKAccessPoint](/documentation/gamekit/gkaccesspoint/shared)

### Managing the location

- [var location: GKAccessPoint.Location](/documentation/gamekit/gkaccesspoint/location-swift.property)
- [GKAccessPoint.Location](/documentation/gamekit/gkaccesspoint/location-swift.enum)

#### Corners

- [case bottomLeading](/documentation/gamekit/gkaccesspoint/location-swift.enum/bottomleading)
- [case bottomTrailing](/documentation/gamekit/gkaccesspoint/location-swift.enum/bottomtrailing)
- [case topLeading](/documentation/gamekit/gkaccesspoint/location-swift.enum/topleading)
- [case topTrailing](/documentation/gamekit/gkaccesspoint/location-swift.enum/toptrailing)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkaccesspoint/location-swift.enum/init(rawvalue:))
- [var frameInScreenCoordinates: CGRect](/documentation/gamekit/gkaccesspoint/frameinscreencoordinates)
- [var parentWindow: UIWindow?](/documentation/gamekit/gkaccesspoint/parentwindow)

### Displaying the access point

- [var isActive: Bool](/documentation/gamekit/gkaccesspoint/isactive)
- [var isPresentingGameCenter: Bool](/documentation/gamekit/gkaccesspoint/ispresentinggamecenter)
- [var isVisible: Bool](/documentation/gamekit/gkaccesspoint/isvisible)
- [var showHighlights: Bool](/documentation/gamekit/gkaccesspoint/showhighlights)

### Managing the access point

- [var isFocused: Bool](/documentation/gamekit/gkaccesspoint/isfocused)
- [func trigger(handler: () -> Void)](/documentation/gamekit/gkaccesspoint/trigger(handler:))
- [func trigger(state: GKGameCenterViewControllerState, handler: () -> Void)](/documentation/gamekit/gkaccesspoint/trigger(state:handler:))
- [func trigger(player: GKPlayer, handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/trigger(player:handler:))
- [func trigger(achievementID: String, handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/trigger(achievementid:handler:))
- [func trigger(leaderboardID: String, playerScope: GKLeaderboard.PlayerScope, timeScope: GKLeaderboard.TimeScope, handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/trigger(leaderboardid:playerscope:timescope:handler:))
- [func trigger(leaderboardSetID: String, handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/trigger(leaderboardsetid:handler:))

### Instance Methods

- [func trigger(challengeDefinitionID: String, handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/trigger(challengedefinitionid:handler:))
- [func trigger(gameActivity: GKGameActivity, handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/trigger(gameactivity:handler:)-6lnz8)
- [func trigger(gameActivity: GKGameActivity, handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/trigger(gameactivity:handler:)-8i6w7)
- [func trigger(gameActivityDefinitionID: String, handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/trigger(gameactivitydefinitionid:handler:)-9hemd)
- [func trigger(gameActivityDefinitionID: String, handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/trigger(gameactivitydefinitionid:handler:)-9m45r)
- [func triggerForArcade(handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/triggerforarcade(handler:))
- [func triggerForChallenges(handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/triggerforchallenges(handler:))
- [func triggerForFriending(handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/triggerforfriending(handler:))
- [func triggerForPlayTogether(handler: (() -> Void)?)](/documentation/gamekit/gkaccesspoint/triggerforplaytogether(handler:))
- [GKDialogController](/documentation/gamekit/gkdialogcontroller)

### Accessing the Shared Dialog Controller

- [class func shared() -> GKDialogController](/documentation/gamekit/gkdialogcontroller/shared())

### Setting the Presentation Window

- [var parentWindow: NSWindow?](/documentation/gamekit/gkdialogcontroller/parentwindow)

### Presenting and Dismissing the Dialog

- [func present(any NSViewController & GKViewController) -> Bool](/documentation/gamekit/gkdialogcontroller/present(_:))
- [func dismiss(Any)](/documentation/gamekit/gkdialogcontroller/dismiss(_:))
- [GKViewController](/documentation/gamekit/gkviewcontroller)

## Leaderboards

- [Encourage progress and competition with leaderboards](/documentation/gamekit/encourage-progress-and-competition-with-leaderboards)
- [Creating recurring leaderboards](/documentation/gamekit/creating-recurring-leaderboards)
- [Adding Recurring Leaderboards to Your Game](/documentation/gamekit/adding-recurring-leaderboards-to-your-game)
- [GKLeaderboard](/documentation/gamekit/gkleaderboard)

### Accessing Identifier and Type Properties

- [var baseLeaderboardID: String](/documentation/gamekit/gkleaderboard/baseleaderboardid)
- [var title: String?](/documentation/gamekit/gkleaderboard/title)
- [var type: GKLeaderboard.LeaderboardType](/documentation/gamekit/gkleaderboard/type)
- [GKLeaderboard.LeaderboardType](/documentation/gamekit/gkleaderboard/leaderboardtype)

#### Constants

- [case classic](/documentation/gamekit/gkleaderboard/leaderboardtype/classic)
- [case recurring](/documentation/gamekit/gkleaderboard/leaderboardtype/recurring)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkleaderboard/leaderboardtype/init(rawvalue:))
- [var groupIdentifier: String?](/documentation/gamekit/gkleaderboard/groupidentifier)

### Accessing Recurring Leaderboard Properties

- [var startDate: Date?](/documentation/gamekit/gkleaderboard/startdate)
- [var nextStartDate: Date?](/documentation/gamekit/gkleaderboard/nextstartdate)
- [var duration: TimeInterval](/documentation/gamekit/gkleaderboard/duration)

### Loading Leaderboards

- [class func loadLeaderboards(IDs: [String]?, completionHandler: ([GKLeaderboard]?, (any Error)?) -> Void)](/documentation/gamekit/gkleaderboard/loadleaderboards(ids:completionhandler:))
- [func loadPreviousOccurrence(completionHandler: (GKLeaderboard?, (any Error)?) -> Void)](/documentation/gamekit/gkleaderboard/loadpreviousoccurrence(completionhandler:))

### Loading Leaderboard Images

- [func loadImage(completionHandler: ((UIImage?, (any Error)?) -> Void)?)](/documentation/gamekit/gkleaderboard/loadimage(completionhandler:))

### Submitting Scores

- [class func submitScore(Int, context: Int, player: GKPlayer, leaderboardIDs: [String], completionHandler: ((any Error)?) -> Void)](/documentation/gamekit/gkleaderboard/submitscore(_:context:player:leaderboardids:completionhandler:))
- [func submitScore(Int, context: Int, player: GKPlayer, completionHandler: ((any Error)?) -> Void)](/documentation/gamekit/gkleaderboard/submitscore(_:context:player:completionhandler:))

### Loading Scores

- [func loadEntries(for: GKLeaderboard.PlayerScope, timeScope: GKLeaderboard.TimeScope, range: NSRange, completionHandler: (GKLeaderboard.Entry?, [GKLeaderboard.Entry]?, Int, (any Error)?) -> Void)](/documentation/gamekit/gkleaderboard/loadentries(for:timescope:range:completionhandler:))
- [func loadEntries(for: [GKPlayer], timeScope: GKLeaderboard.TimeScope, completionHandler: (GKLeaderboard.Entry?, [GKLeaderboard.Entry]?, (any Error)?) -> Void)](/documentation/gamekit/gkleaderboard/loadentries(for:timescope:completionhandler:))
- [GKLeaderboard.PlayerScope](/documentation/gamekit/gkleaderboard/playerscope-swift.enum)

#### Constants

- [case global](/documentation/gamekit/gkleaderboard/playerscope-swift.enum/global)
- [case friendsOnly](/documentation/gamekit/gkleaderboard/playerscope-swift.enum/friendsonly)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkleaderboard/playerscope-swift.enum/init(rawvalue:))
- [GKLeaderboard.TimeScope](/documentation/gamekit/gkleaderboard/timescope-swift.enum)

#### Constants

- [case today](/documentation/gamekit/gkleaderboard/timescope-swift.enum/today)
- [case week](/documentation/gamekit/gkleaderboard/timescope-swift.enum/week)
- [case allTime](/documentation/gamekit/gkleaderboard/timescope-swift.enum/alltime)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkleaderboard/timescope-swift.enum/init(rawvalue:))
- [GKLeaderboard.Entry](/documentation/gamekit/gkleaderboard/entry)

#### Accessing Properties

- [var context: Int](/documentation/gamekit/gkleaderboard/entry/context)
- [var date: Date](/documentation/gamekit/gkleaderboard/entry/date)
- [var formattedScore: String](/documentation/gamekit/gkleaderboard/entry/formattedscore)
- [var player: GKPlayer](/documentation/gamekit/gkleaderboard/entry/player)
- [var rank: Int](/documentation/gamekit/gkleaderboard/entry/rank)
- [var score: Int](/documentation/gamekit/gkleaderboard/entry/score)

#### Presenting Challenges

- [func challengeComposeController(withMessage: String?, players: [GKPlayer]?, completion: GKChallengeComposeHandler?) -> UIViewController](/documentation/gamekit/gkleaderboard/entry/challengecomposecontroller(withmessage:players:completion:))
- [GKChallengeComposeHandler](/documentation/gamekit/gkchallengecomposehandler)
- [func challengeComposeController(withMessage: String?, players: [GKPlayer]?, completionHandler: GKChallengeComposeCompletionBlock?) -> UIViewController](/documentation/gamekit/gkleaderboard/entry/challengecomposecontroller(withmessage:players:completionhandler:))

### Deprecated

- [Deprecated symbols](/documentation/gamekit/gkleaderboard-deprecated-symbols)

#### Deprecated initializers

- [init?(playerIDs: [String]?)](/documentation/gamekit/gkleaderboard/init(playerids:))
- [init(players: [GKPlayer])](/documentation/gamekit/gkleaderboard/init(players:))

#### Deprecated properties

- [var category: String?](/documentation/gamekit/gkleaderboard/category)
- [var identifier: String?](/documentation/gamekit/gkleaderboard/identifier)
- [var isLoading: Bool](/documentation/gamekit/gkleaderboard/isloading)
- [var localPlayerScore: GKScore?](/documentation/gamekit/gkleaderboard/localplayerscore)
- [var maxRange: Int](/documentation/gamekit/gkleaderboard/maxrange)
- [var playerScope: GKLeaderboard.PlayerScope](/documentation/gamekit/gkleaderboard/playerscope-swift.property)
- [var range: NSRange](/documentation/gamekit/gkleaderboard/range)
- [var scores: [GKScore]?](/documentation/gamekit/gkleaderboard/scores)
- [var timeScope: GKLeaderboard.TimeScope](/documentation/gamekit/gkleaderboard/timescope-swift.property)

#### Deprecated methods

- [class func setDefault(String?, withCompletionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkleaderboard/setdefault(_:withcompletionhandler:))
- [class func loadCategories(completionHandler: (([String]?, [String]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkleaderboard/loadcategories(completionhandler:))
- [class func loadLeaderboards(completionHandler: (([GKLeaderboard]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkleaderboard/loadleaderboards(completionhandler:))
- [func loadScores(completionHandler: (([GKScore]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkleaderboard/loadscores(completionhandler:))

### Instance Properties

- [var activityIdentifier: String](/documentation/gamekit/gkleaderboard/activityidentifier)
- [var activityProperties: [String : String]](/documentation/gamekit/gkleaderboard/activityproperties)
- [var isHidden: Bool](/documentation/gamekit/gkleaderboard/ishidden)
- [var leaderboardDescription: String](/documentation/gamekit/gkleaderboard/leaderboarddescription)
- [var releaseState: GKReleaseState](/documentation/gamekit/gkleaderboard/releasestate)
- [GKLeaderboardSet](/documentation/gamekit/gkleaderboardset)

### Accessing Properties

- [var title: String](/documentation/gamekit/gkleaderboardset/title)
- [var identifier: String?](/documentation/gamekit/gkleaderboardset/identifier)
- [var groupIdentifier: String?](/documentation/gamekit/gkleaderboardset/groupidentifier)

### Loading Leaderboard Sets

- [func loadImage(completionHandler: ((UIImage?, (any Error)?) -> Void)?)](/documentation/gamekit/gkleaderboardset/loadimage(completionhandler:))
- [class func loadLeaderboardSets(completionHandler: (([GKLeaderboardSet]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkleaderboardset/loadleaderboardsets(completionhandler:))
- [func loadLeaderboards(handler: ([GKLeaderboard]?, (any Error)?) -> Void)](/documentation/gamekit/gkleaderboardset/loadleaderboards(handler:))
- [func loadLeaderboards(completionHandler: (([GKLeaderboard]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkleaderboardset/loadleaderboards(completionhandler:))
- [GKLeaderboardScore](/documentation/gamekit/gkleaderboardscore)

### Accessing Properties

- [var context: Int](/documentation/gamekit/gkleaderboardscore/context)
- [var leaderboardID: String](/documentation/gamekit/gkleaderboardscore/leaderboardid)
- [var player: GKPlayer](/documentation/gamekit/gkleaderboardscore/player)
- [var value: Int](/documentation/gamekit/gkleaderboardscore/value)

## Achievements

- [Rewarding players with achievements](/documentation/gamekit/rewarding-players-with-achievements)
- [GKAchievement](/documentation/gamekit/gkachievement)

### Loading and Initializing Achievements

- [class func loadAchievements(completionHandler: (([GKAchievement]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkachievement/loadachievements(completionhandler:))
- [init(identifier: String)](/documentation/gamekit/gkachievement/init(identifier:))
- [init(identifier: String, player: GKPlayer)](/documentation/gamekit/gkachievement/init(identifier:player:))

### Accessing Achievement Properties

- [var identifier: String](/documentation/gamekit/gkachievement/identifier)
- [var player: GKPlayer](/documentation/gamekit/gkachievement/player)
- [var percentComplete: Double](/documentation/gamekit/gkachievement/percentcomplete)
- [var isCompleted: Bool](/documentation/gamekit/gkachievement/iscompleted)
- [var lastReportedDate: Date](/documentation/gamekit/gkachievement/lastreporteddate)

### Reporting Progress on Achievements

- [class func report([GKAchievement], withCompletionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkachievement/report(_:withcompletionhandler:))
- [class func report([GKAchievement], withEligibleChallenges: [GKChallenge], withCompletionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkachievement/report(_:witheligiblechallenges:withcompletionhandler:))
- [var showsCompletionBanner: Bool](/documentation/gamekit/gkachievement/showscompletionbanner)
- [class func resetAchievements(completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkachievement/resetachievements(completionhandler:))

### Issuing Achievement Challenges

- [func selectChallengeablePlayers([GKPlayer], withCompletionHandler: (([GKPlayer]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkachievement/selectchallengeableplayers(_:withcompletionhandler:))
- [func challengeComposeController(withMessage: String?, players: [GKPlayer], completion: GKChallengeComposeHandler?) -> UIViewController](/documentation/gamekit/gkachievement/challengecomposecontroller(withmessage:players:completion:))
- [GKChallengeComposeHandler](/documentation/gamekit/gkchallengecomposehandler)
- [func challengeComposeController(withMessage: String?, players: [GKPlayer], completionHandler: GKChallengeComposeCompletionBlock?) -> UIViewController](/documentation/gamekit/gkachievement/challengecomposecontroller(withmessage:players:completionhandler:))
- [func challengeComposeController(withPlayers: [String]?, message: String?, completionHandler: GKChallengeComposeCompletionBlock?) -> UIViewController?](/documentation/gamekit/gkachievement/challengecomposecontroller(withplayers:message:completionhandler:))

### Deprecated

- [Deprecated Symbols](/documentation/gamekit/gkachievement-deprecated-symbols)

#### Deprecated Initializers

- [init?(identifier: String?, forPlayer: String)](/documentation/gamekit/gkachievement/init(identifier:forplayer:))

#### Deprecated Methods

- [func issueChallenge(toPlayers: [String]?, message: String?)](/documentation/gamekit/gkachievement/issuechallenge(toplayers:message:))
- [func report(completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkachievement/report(completionhandler:))
- [func selectChallengeablePlayerIDs([String]?, withCompletionHandler: (([String]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkachievement/selectchallengeableplayerids(_:withcompletionhandler:))

#### Deprecated Properties

- [var isHidden: Bool](/documentation/gamekit/gkachievement/ishidden)
- [var playerID: String?](/documentation/gamekit/gkachievement/playerid)
- [GKAchievementDescription](/documentation/gamekit/gkachievementdescription)

### Retrieving Achievement Descriptions

- [class func loadAchievementDescriptions(completionHandler: (([GKAchievementDescription]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkachievementdescription/loadachievementdescriptions(completionhandler:))

### Reading and Writing Achievement Properties

- [var identifier: String](/documentation/gamekit/gkachievementdescription/identifier)
- [var title: String](/documentation/gamekit/gkachievementdescription/title)
- [var unachievedDescription: String](/documentation/gamekit/gkachievementdescription/unachieveddescription)
- [var achievedDescription: String](/documentation/gamekit/gkachievementdescription/achieveddescription)
- [var maximumPoints: Int](/documentation/gamekit/gkachievementdescription/maximumpoints)
- [var image: NSImage?](/documentation/gamekit/gkachievementdescription/image)
- [var isHidden: Bool](/documentation/gamekit/gkachievementdescription/ishidden)
- [var isReplayable: Bool](/documentation/gamekit/gkachievementdescription/isreplayable)
- [var rarityPercent: Double?](/documentation/gamekit/gkachievementdescription/raritypercent-4bh6k)

### Working with Achievement Images

- [class func incompleteAchievementImage() -> UIImage](/documentation/gamekit/gkachievementdescription/incompleteachievementimage())
- [class func placeholderCompletedAchievementImage() -> UIImage](/documentation/gamekit/gkachievementdescription/placeholdercompletedachievementimage())
- [func loadImage(completionHandler: ((UIImage?, (any Error)?) -> Void)?)](/documentation/gamekit/gkachievementdescription/loadimage(completionhandler:))

### Retrieving Group Information

- [var groupIdentifier: String?](/documentation/gamekit/gkachievementdescription/groupidentifier)

### Instance Properties

- [var activityIdentifier: String](/documentation/gamekit/gkachievementdescription/activityidentifier)
- [var activityProperties: [String : String]](/documentation/gamekit/gkachievementdescription/activityproperties)
- [var releaseState: GKReleaseState](/documentation/gamekit/gkachievementdescription/releasestate)

## Challenges

- [Creating engaging challenges from leaderboards](/documentation/gamekit/creating-engaging-challenges-from-leaderboards)
- [Choosing a leaderboard for your challenges](/documentation/gamekit/choosing-a-leaderboard-for-your-challenges)
- [GKChallengeDefinition](/documentation/gamekit/gkchallengedefinition)

### Getting the display properties and image

- [var title: String](/documentation/gamekit/gkchallengedefinition/title)
- [var details: String?](/documentation/gamekit/gkchallengedefinition/details)
- [func loadImage(completionHandler: (UIImage?, (any Error)?) -> Void)](/documentation/gamekit/gkchallengedefinition/loadimage(completionhandler:))

### Getting the challenge rules

- [var durationOptions: [DateComponents]](/documentation/gamekit/gkchallengedefinition/durationoptions)
- [var isRepeatable: Bool](/documentation/gamekit/gkchallengedefinition/isrepeatable)

### Getting the leaderboard

- [var leaderboard: GKLeaderboard?](/documentation/gamekit/gkchallengedefinition/leaderboard)

### Getting the release state

- [var releaseState: GKReleaseState](/documentation/gamekit/gkchallengedefinition/releasestate)
- [GKReleaseState](/documentation/gamekit/gkreleasestate)

#### Initializers

- [init(rawValue: UInt)](/documentation/gamekit/gkreleasestate/init(rawvalue:))

#### Type Properties

- [static var prereleased: GKReleaseState](/documentation/gamekit/gkreleasestate/prereleased)
- [static var released: GKReleaseState](/documentation/gamekit/gkreleasestate/released)

### Getting the identifier properties

- [var groupIdentifier: String?](/documentation/gamekit/gkchallengedefinition/groupidentifier)
- [var identifier: String](/documentation/gamekit/gkchallengedefinition/identifier)

### Loading challenge definitions

- [class func loadChallengeDefinitions(completionHandler: ([GKChallengeDefinition]?, (any Error)?) -> Void)](/documentation/gamekit/gkchallengedefinition/loadchallengedefinitions(completionhandler:))

### Checking for active challenges

- [func hasActiveChallenges(completionHandler: (Bool, (any Error)?) -> Void)](/documentation/gamekit/gkchallengedefinition/hasactivechallenges(completionhandler:))
- [GKShowChallengeBanners](/documentation/bundleresources/information-property-list/gkshowchallengebanners)

## Activities

- [Creating activities for your game](/documentation/gamekit/creating-activities-for-your-game)
- [GKGameActivity](/documentation/gamekit/gkgameactivity)

### Creating an activity

- [init(definition: GKGameActivityDefinition)](/documentation/gamekit/gkgameactivity/init(definition:))
- [class func start(definition: GKGameActivityDefinition) throws -> GKGameActivity](/documentation/gamekit/gkgameactivity/start(definition:))
- [class func start(definition: GKGameActivityDefinition, partyCode: String) throws -> GKGameActivity](/documentation/gamekit/gkgameactivity/start(definition:partycode:))

### Getting the activity definition

- [var activityDefinition: GKGameActivityDefinition](/documentation/gamekit/gkgameactivity/activitydefinition)

### Getting the activity state

- [var state: GKGameActivity.State](/documentation/gamekit/gkgameactivity/state-swift.property)
- [GKGameActivity.State](/documentation/gamekit/gkgameactivity/state-swift.enum)

#### Enumeration Cases

- [case active](/documentation/gamekit/gkgameactivity/state-swift.enum/active)
- [case ended](/documentation/gamekit/gkgameactivity/state-swift.enum/ended)
- [case initialized](/documentation/gamekit/gkgameactivity/state-swift.enum/initialized)
- [case paused](/documentation/gamekit/gkgameactivity/state-swift.enum/paused)

#### Initializers

- [init?(rawValue: UInt)](/documentation/gamekit/gkgameactivity/state-swift.enum/init(rawvalue:))

### Updating the activity state

- [func start()](/documentation/gamekit/gkgameactivity/start())
- [func pause()](/documentation/gamekit/gkgameactivity/pause())
- [func resume()](/documentation/gamekit/gkgameactivity/resume())
- [func end()](/documentation/gamekit/gkgameactivity/end())

### Getting and removing achievements

- [var achievements: Set<GKAchievement>](/documentation/gamekit/gkgameactivity/achievements)
- [func removeAchievements([GKAchievement])](/documentation/gamekit/gkgameactivity/removeachievements(_:))
- [func progress(on: GKAchievement) -> Double](/documentation/gamekit/gkgameactivity/progress(on:))
- [func setProgress(on: GKAchievement, to: Double)](/documentation/gamekit/gkgameactivity/setprogress(on:to:))
- [func setAchievementCompleted(GKAchievement)](/documentation/gamekit/gkgameactivity/setachievementcompleted(_:))

### Getting and removing leaderboard scores

- [var leaderboardScores: Set<GKLeaderboardScore>](/documentation/gamekit/gkgameactivity/leaderboardscores)
- [func score(on: GKLeaderboard) -> GKLeaderboardScore?](/documentation/gamekit/gkgameactivity/score(on:))
- [func setScore(on: GKLeaderboard, to: Int)](/documentation/gamekit/gkgameactivity/setscore(on:to:))
- [func setScore(on: GKLeaderboard, to: Int, context: Int)](/documentation/gamekit/gkgameactivity/setscore(on:to:context:))
- [func removeScores(from: [GKLeaderboard])](/documentation/gamekit/gkgameactivity/removescores(from:))

### Getting and verifying the party code

- [var partyCode: String?](/documentation/gamekit/gkgameactivity/partycode)
- [var partyURL: URL?](/documentation/gamekit/gkgameactivity/partyurl)
- [class var validPartyCodeAlphabet: [String]](/documentation/gamekit/gkgameactivity/validpartycodealphabet)
- [class func isValidPartyCode(String) -> Bool](/documentation/gamekit/gkgameactivity/isvalidpartycode(_:))

### Getting the activity properties

- [var duration: TimeInterval](/documentation/gamekit/gkgameactivity/duration)
- [var startDate: Date?](/documentation/gamekit/gkgameactivity/startdate)
- [var endDate: Date?](/documentation/gamekit/gkgameactivity/enddate)
- [var creationDate: Date](/documentation/gamekit/gkgameactivity/creationdate)
- [var lastResumeDate: Date?](/documentation/gamekit/gkgameactivity/lastresumedate)

### Getting the custom user data

- [var properties: [String : String]](/documentation/gamekit/gkgameactivity/properties)

### Getting the activity identifiers

- [var identifier: String](/documentation/gamekit/gkgameactivity/identifier)

### Checking for an activity

- [class func checkPendingGameActivityExistence(completionHandler: (Bool) -> Void)](/documentation/gamekit/gkgameactivity/checkpendinggameactivityexistence(completionhandler:))

### Creating a matchmaking request

- [func makeMatchRequest() -> GKMatchRequest?](/documentation/gamekit/gkgameactivity/makematchrequest())

### Performing a matchmaking request

- [func findMatch(completionHandler: (GKMatch?, (any Error)?) -> Void)](/documentation/gamekit/gkgameactivity/findmatch(completionhandler:))
- [func findPlayersForHostedMatch(completionHandler: ([GKPlayer]?, (any Error)?) -> Void)](/documentation/gamekit/gkgameactivity/findplayersforhostedmatch(completionhandler:))
- [GKGameActivityDefinition](/documentation/gamekit/gkgameactivitydefinition)

### Getting the display properties and image

- [var title: String](/documentation/gamekit/gkgameactivitydefinition/title)
- [var details: String?](/documentation/gamekit/gkgameactivitydefinition/details)
- [var defaultProperties: [String : String]](/documentation/gamekit/gkgameactivitydefinition/defaultproperties)
- [func loadImage(completionHandler: (UIImage?, (any Error)?) -> Void)](/documentation/gamekit/gkgameactivitydefinition/loadimage(completionhandler:))

### Getting the activity capabilities

- [var supportsPartyCode: Bool](/documentation/gamekit/gkgameactivitydefinition/supportspartycode)
- [var supportsUnlimitedPlayers: Bool](/documentation/gamekit/gkgameactivitydefinition/supportsunlimitedplayers)
- [var playerRange: (any RangeExpression)?](/documentation/gamekit/gkgameactivitydefinition/playerrange)
- [var playStyle: GKGameActivityPlayStyle](/documentation/gamekit/gkgameactivitydefinition/playstyle)
- [GKGameActivityPlayStyle](/documentation/gamekit/gkgameactivityplaystyle)

#### Enumeration Cases

- [case asynchronous](/documentation/gamekit/gkgameactivityplaystyle/asynchronous)
- [case synchronous](/documentation/gamekit/gkgameactivityplaystyle/synchronous)
- [case unspecified](/documentation/gamekit/gkgameactivityplaystyle/unspecified)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkgameactivityplaystyle/init(rawvalue:))

### Getting the fallback URL

- [var fallbackURL: URL?](/documentation/gamekit/gkgameactivitydefinition/fallbackurl)

### Getting the release state

- [var releaseState: GKReleaseState](/documentation/gamekit/gkgameactivitydefinition/releasestate)
- [GKReleaseState](/documentation/gamekit/gkreleasestate)

#### Initializers

- [init(rawValue: UInt)](/documentation/gamekit/gkreleasestate/init(rawvalue:))

#### Type Properties

- [static var prereleased: GKReleaseState](/documentation/gamekit/gkreleasestate/prereleased)
- [static var released: GKReleaseState](/documentation/gamekit/gkreleasestate/released)

### Getting the identifier properties

- [var identifier: String](/documentation/gamekit/gkgameactivitydefinition/identifier)
- [var groupIdentifier: String?](/documentation/gamekit/gkgameactivitydefinition/groupidentifier)

### Loading activity definitions

- [class func loadGameActivityDefinitions(completionHandler: ([GKGameActivityDefinition]?, (any Error)?) -> Void)](/documentation/gamekit/gkgameactivitydefinition/loadgameactivitydefinitions(completionhandler:))

### Loading achievement descriptions

- [func loadAchievementDescriptions(completionHandler: ([GKAchievementDescription]?, (any Error)?) -> Void)](/documentation/gamekit/gkgameactivitydefinition/loadachievementdescriptions(completionhandler:))

### Loading leaderboards

- [func loadLeaderboards(completionHandler: ([GKLeaderboard]?, (any Error)?) -> Void)](/documentation/gamekit/gkgameactivitydefinition/loadleaderboards(completionhandler:))

### Type Methods

- [class func loadGameActivityDefinitions(IDs: [String]?, completionHandler: ([GKGameActivityDefinition]?, (any Error)?) -> Void)](/documentation/gamekit/gkgameactivitydefinition/loadgameactivitydefinitions(ids:completionhandler:))
- [GKGameActivityListener](/documentation/gamekit/gkgameactivitylistener)

### Responding to an activity

- [func player(GKPlayer, wantsToPlay: GKGameActivity, completionHandler: (Bool) -> Void)](/documentation/gamekit/gkgameactivitylistener/player(_:wantstoplay:completionhandler:))

## Real-time games

- [Creating real-time games](/documentation/gamekit/creating-real-time-games)
- [Finding multiple players for a game](/documentation/gamekit/finding-multiple-players-for-a-game)
- [Exchanging data between players in real-time games](/documentation/gamekit/exchanging-data-between-players-in-real-time-games)
- [Adding voice chat to multiplayer games](/documentation/gamekit/adding-voice-chat-to-multiplayer-games)
- [Finding players for custom server-based games](/documentation/gamekit/finding-players-for-custom-server-based-games)
- [Matchmaking rules](/documentation/gamekit/matchmaking-rules)

### Essentials

- [Finding players using matchmaking rules](/documentation/gamekit/finding-players-using-matchmaking-rules)

### Rules

- [Letting players join matches using party codes](/documentation/gamekit/letting-players-join-matches-using-party-codes)
- [Finding players with similar skill levels](/documentation/gamekit/finding-players-with-similar-skill-levels)
- [Assigning players to teams using rules](/documentation/gamekit/assigning-players-to-teams-using-rules)
- [Creating matchmaking rules for backward compatibility](/documentation/gamekit/creating-matchmaking-rules-for-backward-compatibility)

### Testing

- [Testing matchmaking rules](/documentation/gamekit/testing-matchmaking-rules)
- [Troubleshooting matchmaking rules using metrics](/documentation/gamekit/troubleshooting-matchmaking-rules-using-metrics)
- [Testing rule sets with player traffic using metrics](/documentation/gamekit/testing-rule-sets-with-player-traffic-using-metrics)
- [GKMatchRequest](/documentation/gamekit/gkmatchrequest)

### Restricting the number of players

- [class func maxPlayersAllowedForMatch(of: GKMatchType) -> Int](/documentation/gamekit/gkmatchrequest/maxplayersallowedformatch(of:))
- [GKMatchType](/documentation/gamekit/gkmatchtype)

#### Types

- [case peerToPeer](/documentation/gamekit/gkmatchtype/peertopeer)
- [case hosted](/documentation/gamekit/gkmatchtype/hosted)
- [case turnBased](/documentation/gamekit/gkmatchtype/turnbased)

#### Initializers

- [init?(rawValue: UInt)](/documentation/gamekit/gkmatchtype/init(rawvalue:))
- [var minPlayers: Int](/documentation/gamekit/gkmatchrequest/minplayers)
- [var maxPlayers: Int](/documentation/gamekit/gkmatchrequest/maxplayers)
- [var defaultNumberOfPlayers: Int](/documentation/gamekit/gkmatchrequest/defaultnumberofplayers)

### Inviting players

- [var inviteMessage: String?](/documentation/gamekit/gkmatchrequest/invitemessage)
- [var recipients: [GKPlayer]?](/documentation/gamekit/gkmatchrequest/recipients)
- [var recipientResponseHandler: ((GKPlayer, GKInviteRecipientResponse) -> Void)?](/documentation/gamekit/gkmatchrequest/recipientresponsehandler)
- [GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse)

#### Responses

- [case accepted](/documentation/gamekit/gkinviterecipientresponse/accepted)
- [case declined](/documentation/gamekit/gkinviterecipientresponse/declined)
- [case failed](/documentation/gamekit/gkinviterecipientresponse/failed)
- [case incompatible](/documentation/gamekit/gkinviterecipientresponse/incompatible)
- [case unableToConnect](/documentation/gamekit/gkinviterecipientresponse/unabletoconnect)
- [case noAnswer](/documentation/gamekit/gkinviterecipientresponse/noanswer)

#### Deprecated Properties

- [static var inviteeResponseAccepted: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponseaccepted)
- [static var inviteeResponseDeclined: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponsedeclined)
- [static var inviteeResponseFailed: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponsefailed)
- [static var inviteeResponseIncompatible: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponseincompatible)
- [static var inviteeResponseNoAnswer: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponsenoanswer)
- [static var inviteeResponseUnableToConnect: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponseunabletoconnect)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkinviterecipientresponse/init(rawvalue:))

### Matching players using rules

- [var queueName: String?](/documentation/gamekit/gkmatchrequest/queuename)
- [var properties: [String : Any]?](/documentation/gamekit/gkmatchrequest/properties)
- [var recipientProperties: [GKPlayer : [String : Any]]?](/documentation/gamekit/gkmatchrequest/recipientproperties)

### Matching specific players

- [var playerGroup: Int](/documentation/gamekit/gkmatchrequest/playergroup)
- [var playerAttributes: UInt32](/documentation/gamekit/gkmatchrequest/playerattributes)

### Deprecated methods and properties

- [var inviteeResponseHandler: ((String, GKInviteeResponse) -> Void)?](/documentation/gamekit/gkmatchrequest/inviteeresponsehandler)
- [GKInviteeResponse](/documentation/gamekit/gkinviteeresponse)

#### Responses

- [static var inviteeResponseAccepted: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponseaccepted)
- [static var inviteeResponseDeclined: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponsedeclined)
- [static var inviteeResponseFailed: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponsefailed)
- [static var inviteeResponseIncompatible: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponseincompatible)
- [static var inviteeResponseUnableToConnect: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponseunabletoconnect)
- [static var inviteeResponseNoAnswer: GKInviteRecipientResponse](/documentation/gamekit/gkinviterecipientresponse/inviteeresponsenoanswer)
- [var playersToInvite: [String]?](/documentation/gamekit/gkmatchrequest/playerstoinvite)
- [var restrictToAutomatch: Bool](/documentation/gamekit/gkmatchrequest/restricttoautomatch)
- [GKMatchmaker](/documentation/gamekit/gkmatchmaker)

### Retrieving the shared matchmaker

- [class func shared() -> GKMatchmaker](/documentation/gamekit/gkmatchmaker/shared())

### Receiving invitations from other players

- [func match(for: GKInvite, completionHandler: ((GKMatch?, (any Error)?) -> Void)?)](/documentation/gamekit/gkmatchmaker/match(for:completionhandler:))

### Matching players

- [func findMatch(for: GKMatchRequest, withCompletionHandler: ((GKMatch?, (any Error)?) -> Void)?)](/documentation/gamekit/gkmatchmaker/findmatch(for:withcompletionhandler:))
- [func findPlayers(forHostedRequest: GKMatchRequest, withCompletionHandler: (([GKPlayer]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkmatchmaker/findplayers(forhostedrequest:withcompletionhandler:))
- [func findMatchedPlayers(GKMatchRequest, withCompletionHandler: (GKMatchedPlayers?, (any Error)?) -> Void)](/documentation/gamekit/gkmatchmaker/findmatchedplayers(_:withcompletionhandler:))
- [GKMatchedPlayers](/documentation/gamekit/gkmatchedplayers)

#### Getting players

- [var players: [GKPlayer]](/documentation/gamekit/gkmatchedplayers/players)

#### Matchmaking using rules

- [var properties: [String : Any]?](/documentation/gamekit/gkmatchedplayers/properties)
- [var playerProperties: [GKPlayer : [String : Any]]?](/documentation/gamekit/gkmatchedplayers/playerproperties)
- [func addPlayers(to: GKMatch, matchRequest: GKMatchRequest, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkmatchmaker/addplayers(to:matchrequest:completionhandler:))
- [func finishMatchmaking(for: GKMatch)](/documentation/gamekit/gkmatchmaker/finishmatchmaking(for:))
- [func cancel()](/documentation/gamekit/gkmatchmaker/cancel())
- [func cancelPendingInvite(to: GKPlayer)](/documentation/gamekit/gkmatchmaker/cancelpendinginvite(to:))

### Finding players who request matches

- [func queryActivity(completionHandler: ((Int, (any Error)?) -> Void)?)](/documentation/gamekit/gkmatchmaker/queryactivity(completionhandler:))
- [func queryPlayerGroupActivity(Int, withCompletionHandler: ((Int, (any Error)?) -> Void)?)](/documentation/gamekit/gkmatchmaker/queryplayergroupactivity(_:withcompletionhandler:))
- [func queryQueueActivity(String, withCompletionHandler: ((Int, (any Error)?) -> Void)?)](/documentation/gamekit/gkmatchmaker/queryqueueactivity(_:withcompletionhandler:))

### Looking for nearby players

- [func startBrowsingForNearbyPlayers(handler: ((GKPlayer, Bool) -> Void)?)](/documentation/gamekit/gkmatchmaker/startbrowsingfornearbyplayers(handler:))
- [func stopBrowsingForNearbyPlayers()](/documentation/gamekit/gkmatchmaker/stopbrowsingfornearbyplayers())

### Starting matches using SharePlay

- [func startGroupActivity(playerHandler: (GKPlayer) -> Void)](/documentation/gamekit/gkmatchmaker/startgroupactivity(playerhandler:))
- [func stopGroupActivity()](/documentation/gamekit/gkmatchmaker/stopgroupactivity())

### Deprecated

- [Deprecated Symbols](/documentation/gamekit/gkmatchmaker-deprecated-symbols)

#### Deprecated Properties

- [var inviteHandler: ((GKInvite, [Any]?) -> Void)?](/documentation/gamekit/gkmatchmaker/invitehandler)

#### Deprecated Methods

- [func cancelInvite(toPlayer: String)](/documentation/gamekit/gkmatchmaker/cancelinvite(toplayer:))
- [func findPlayers(forHostedMatchRequest: GKMatchRequest, withCompletionHandler: (([String]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkmatchmaker/findplayers(forhostedmatchrequest:withcompletionhandler:))
- [func startBrowsingForNearbyPlayers(reachableHandler: ((String, Bool) -> Void)?)](/documentation/gamekit/gkmatchmaker/startbrowsingfornearbyplayers(reachablehandler:))
- [GKMatchmakerViewController](/documentation/gamekit/gkmatchmakerviewcontroller)

### Creating and configuring the view controller

- [init?(matchRequest: GKMatchRequest)](/documentation/gamekit/gkmatchmakerviewcontroller/init(matchrequest:))
- [init?(invite: GKInvite)](/documentation/gamekit/gkmatchmakerviewcontroller/init(invite:))
- [var matchRequest: GKMatchRequest](/documentation/gamekit/gkmatchmakerviewcontroller/matchrequest)
- [var canStartWithMinimumPlayers: Bool](/documentation/gamekit/gkmatchmakerviewcontroller/canstartwithminimumplayers)
- [var matchmakingMode: GKMatchmakingMode](/documentation/gamekit/gkmatchmakerviewcontroller/matchmakingmode)
- [GKMatchmakingMode](/documentation/gamekit/gkmatchmakingmode)

#### Modes

- [case `default`](/documentation/gamekit/gkmatchmakingmode/default)
- [case nearbyOnly](/documentation/gamekit/gkmatchmakingmode/nearbyonly)
- [case automatchOnly](/documentation/gamekit/gkmatchmakingmode/automatchonly)
- [case inviteOnly](/documentation/gamekit/gkmatchmakingmode/inviteonly)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkmatchmakingmode/init(rawvalue:))

### Setting the delegate

- [var matchmakerDelegate: (any GKMatchmakerViewControllerDelegate)?](/documentation/gamekit/gkmatchmakerviewcontroller/matchmakerdelegate)
- [GKMatchmakerViewControllerDelegate](/documentation/gamekit/gkmatchmakerviewcontrollerdelegate)

#### Starting matches

- [func matchmakerViewController(GKMatchmakerViewController, didFind: GKMatch)](/documentation/gamekit/gkmatchmakerviewcontrollerdelegate/matchmakerviewcontroller(_:didfind:))
- [func matchmakerViewController(GKMatchmakerViewController, didFindHostedPlayers: [GKPlayer])](/documentation/gamekit/gkmatchmakerviewcontrollerdelegate/matchmakerviewcontroller(_:didfindhostedplayers:))

#### Matching players using rules

- [func matchmakerViewController(GKMatchmakerViewController, getMatchPropertiesForRecipient: GKPlayer, withCompletionHandler: ([String : Any]) -> Void)](/documentation/gamekit/gkmatchmakerviewcontrollerdelegate/matchmakerviewcontroller(_:getmatchpropertiesforrecipient:withcompletionhandler:))

#### Handling cancellations and errors

- [func matchmakerViewControllerWasCancelled(GKMatchmakerViewController)](/documentation/gamekit/gkmatchmakerviewcontrollerdelegate/matchmakerviewcontrollerwascancelled(_:))
- [func matchmakerViewController(GKMatchmakerViewController, didFailWithError: any Error)](/documentation/gamekit/gkmatchmakerviewcontrollerdelegate/matchmakerviewcontroller(_:didfailwitherror:))

#### Hosting matches

- [func matchmakerViewController(GKMatchmakerViewController, hostedPlayerDidAccept: GKPlayer)](/documentation/gamekit/gkmatchmakerviewcontrollerdelegate/matchmakerviewcontroller(_:hostedplayerdidaccept:))

#### Deprecated Methods

- [func matchmakerViewController(GKMatchmakerViewController, didFindPlayers: [String])](/documentation/gamekit/gkmatchmakerviewcontrollerdelegate/matchmakerviewcontroller(_:didfindplayers:))
- [func matchmakerViewController(GKMatchmakerViewController, didReceiveAcceptFromHostedPlayer: String)](/documentation/gamekit/gkmatchmakerviewcontrollerdelegate/matchmakerviewcontroller(_:didreceiveacceptfromhostedplayer:))

### Adding players to matches

- [func addPlayers(to: GKMatch)](/documentation/gamekit/gkmatchmakerviewcontroller/addplayers(to:))

### Hosting matches

- [var isHosted: Bool](/documentation/gamekit/gkmatchmakerviewcontroller/ishosted)
- [func setHostedPlayer(GKPlayer, didConnect: Bool)](/documentation/gamekit/gkmatchmakerviewcontroller/sethostedplayer(_:didconnect:))

### Deprecated

- [func setHostedPlayer(String, connected: Bool)](/documentation/gamekit/gkmatchmakerviewcontroller/sethostedplayer(_:connected:))
- [func setHostedPlayerReady(String)](/documentation/gamekit/gkmatchmakerviewcontroller/sethostedplayerready(_:))
- [var defaultInvitationMessage: String?](/documentation/gamekit/gkmatchmakerviewcontroller/defaultinvitationmessage)
- [GKInviteEventListener](/documentation/gamekit/gkinviteeventlistener)

### Starting a New Match

- [func player(GKPlayer, didAccept: GKInvite)](/documentation/gamekit/gkinviteeventlistener/player(_:didaccept:))
- [func player(GKPlayer, didRequestMatchWithRecipients: [GKPlayer])](/documentation/gamekit/gkinviteeventlistener/player(_:didrequestmatchwithrecipients:))
- [func player(GKPlayer, didRequestMatchWithPlayers: [String])](/documentation/gamekit/gkinviteeventlistener/player(_:didrequestmatchwithplayers:))
- [GKInvite](/documentation/gamekit/gkinvite)

### Getting Properties

- [var sender: GKPlayer](/documentation/gamekit/gkinvite/sender)
- [var playerAttributes: UInt32](/documentation/gamekit/gkinvite/playerattributes)
- [var playerGroup: Int](/documentation/gamekit/gkinvite/playergroup)
- [var isHosted: Bool](/documentation/gamekit/gkinvite/ishosted)
- [var inviter: String](/documentation/gamekit/gkinvite/inviter)
- [GKMatch](/documentation/gamekit/gkmatch)

### Setting the delegate

- [var delegate: (any GKMatchDelegate)?](/documentation/gamekit/gkmatch/delegate)
- [GKMatchDelegate](/documentation/gamekit/gkmatchdelegate)

#### Receiving Data from Other Players

- [func match(GKMatch, didReceive: Data, forRecipient: GKPlayer, fromRemotePlayer: GKPlayer)](/documentation/gamekit/gkmatchdelegate/match(_:didreceive:forrecipient:fromremoteplayer:))
- [func match(GKMatch, didReceive: Data, fromRemotePlayer: GKPlayer)](/documentation/gamekit/gkmatchdelegate/match(_:didreceive:fromremoteplayer:))

#### Receiving State Notifications About Other Players

- [func match(GKMatch, player: GKPlayer, didChange: GKPlayerConnectionState)](/documentation/gamekit/gkmatchdelegate/match(_:player:didchange:)-8ohgr)
- [GKPlayerConnectionState](/documentation/gamekit/gkplayerconnectionstate)

##### States

- [case unknown](/documentation/gamekit/gkplayerconnectionstate/unknown)
- [case connected](/documentation/gamekit/gkplayerconnectionstate/connected)
- [case disconnected](/documentation/gamekit/gkplayerconnectionstate/disconnected)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkplayerconnectionstate/init(rawvalue:))

#### Handling Errors

- [func match(GKMatch, didFailWithError: (any Error)?)](/documentation/gamekit/gkmatchdelegate/match(_:didfailwitherror:))

#### Reinviting a Player

- [func match(GKMatch, shouldReinviteDisconnectedPlayer: GKPlayer) -> Bool](/documentation/gamekit/gkmatchdelegate/match(_:shouldreinvitedisconnectedplayer:))

#### Deprecated Methods and Properties

- [func match(GKMatch, player: String, didChange: GKPlayerConnectionState)](/documentation/gamekit/gkmatchdelegate/match(_:player:didchange:)-4eo7p)
- [func match(GKMatch, didReceive: Data, fromPlayer: String)](/documentation/gamekit/gkmatchdelegate/match(_:didreceive:fromplayer:))
- [func match(GKMatch, shouldReinvitePlayer: String) -> Bool](/documentation/gamekit/gkmatchdelegate/match(_:shouldreinviteplayer:))

### Working with other players

- [var expectedPlayerCount: Int](/documentation/gamekit/gkmatch/expectedplayercount)
- [var players: [GKPlayer]](/documentation/gamekit/gkmatch/players)

### Sending data to other players

- [func chooseBestHostingPlayer(completionHandler: (GKPlayer?) -> Void)](/documentation/gamekit/gkmatch/choosebesthostingplayer(completionhandler:))
- [func send(Data, to: [GKPlayer], dataMode: GKMatch.SendDataMode) throws](/documentation/gamekit/gkmatch/send(_:to:datamode:))
- [func sendData(toAllPlayers: Data, with: GKMatch.SendDataMode) throws](/documentation/gamekit/gkmatch/senddata(toallplayers:with:))
- [GKMatch.SendDataMode](/documentation/gamekit/gkmatch/senddatamode)

#### Modes

- [case reliable](/documentation/gamekit/gkmatch/senddatamode/reliable)
- [case unreliable](/documentation/gamekit/gkmatch/senddatamode/unreliable)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkmatch/senddatamode/init(rawvalue:))

### Joining a voice chat

- [func voiceChat(withName: String) -> GKVoiceChat?](/documentation/gamekit/gkmatch/voicechat(withname:))

### Getting matchmaking properties

- [var properties: [String : Any]?](/documentation/gamekit/gkmatch/properties)
- [var playerProperties: [GKPlayer : [String : Any]]?](/documentation/gamekit/gkmatch/playerproperties)

### Finishing the match

- [func disconnect()](/documentation/gamekit/gkmatch/disconnect())
- [func rematch(completionHandler: ((GKMatch?, (any Error)?) -> Void)?)](/documentation/gamekit/gkmatch/rematch(completionhandler:))

### Deprecated Methods and Properties

- [func chooseBestHostPlayer(completionHandler: (String?) -> Void)](/documentation/gamekit/gkmatch/choosebesthostplayer(completionhandler:))
- [var playerIDs: [String]?](/documentation/gamekit/gkmatch/playerids)
- [func send(Data, toPlayers: [String], with: GKMatch.SendDataMode) throws](/documentation/gamekit/gkmatch/send(_:toplayers:with:))

## Turn-based games

- [Creating turn-based games](/documentation/gamekit/creating-turn-based-games)
- [Starting turn-based matches and passing turns between players](/documentation/gamekit/starting-turn-based-matches-and-passing-turns-between-players)
- [Sending messages to players in turn-based games](/documentation/gamekit/sending-messages-to-players-in-turn-based-games)
- [Exchanging data between players in turn-based games](/documentation/gamekit/exchanging-data-between-players-in-turn-based-games)
- [GKTurnBasedMatchmakerViewController](/documentation/gamekit/gkturnbasedmatchmakerviewcontroller)

### Creating and Configuring the View Controller

- [init(matchRequest: GKMatchRequest)](/documentation/gamekit/gkturnbasedmatchmakerviewcontroller/init(matchrequest:))
- [var showExistingMatches: Bool](/documentation/gamekit/gkturnbasedmatchmakerviewcontroller/showexistingmatches)
- [var matchmakingMode: GKMatchmakingMode](/documentation/gamekit/gkturnbasedmatchmakerviewcontroller/matchmakingmode)
- [GKMatchmakingMode](/documentation/gamekit/gkmatchmakingmode)

#### Modes

- [case `default`](/documentation/gamekit/gkmatchmakingmode/default)
- [case nearbyOnly](/documentation/gamekit/gkmatchmakingmode/nearbyonly)
- [case automatchOnly](/documentation/gamekit/gkmatchmakingmode/automatchonly)
- [case inviteOnly](/documentation/gamekit/gkmatchmakingmode/inviteonly)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkmatchmakingmode/init(rawvalue:))

### Setting the Delegate

- [var turnBasedMatchmakerDelegate: (any GKTurnBasedMatchmakerViewControllerDelegate)?](/documentation/gamekit/gkturnbasedmatchmakerviewcontroller/turnbasedmatchmakerdelegate)
- [GKTurnBasedMatchmakerViewControllerDelegate](/documentation/gamekit/gkturnbasedmatchmakerviewcontrollerdelegate)

#### Handling Cancellation and Errors

- [func turnBasedMatchmakerViewControllerWasCancelled(GKTurnBasedMatchmakerViewController)](/documentation/gamekit/gkturnbasedmatchmakerviewcontrollerdelegate/turnbasedmatchmakerviewcontrollerwascancelled(_:))
- [func turnBasedMatchmakerViewController(GKTurnBasedMatchmakerViewController, didFailWithError: any Error)](/documentation/gamekit/gkturnbasedmatchmakerviewcontrollerdelegate/turnbasedmatchmakerviewcontroller(_:didfailwitherror:))

#### Deprecated Methods

- [func turnBasedMatchmakerViewController(GKTurnBasedMatchmakerViewController, didFind: GKTurnBasedMatch)](/documentation/gamekit/gkturnbasedmatchmakerviewcontrollerdelegate/turnbasedmatchmakerviewcontroller(_:didfind:))
- [func turnBasedMatchmakerViewController(GKTurnBasedMatchmakerViewController, playerQuitFor: GKTurnBasedMatch)](/documentation/gamekit/gkturnbasedmatchmakerviewcontrollerdelegate/turnbasedmatchmakerviewcontroller(_:playerquitfor:))
- [GKTurnBasedMatch](/documentation/gamekit/gkturnbasedmatch)

### Creating a Match

- [class func find(for: GKMatchRequest, withCompletionHandler: (GKTurnBasedMatch?, (any Error)?) -> Void)](/documentation/gamekit/gkturnbasedmatch/find(for:withcompletionhandler:))
- [func acceptInvite(completionHandler: ((GKTurnBasedMatch?, (any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/acceptinvite(completionhandler:))
- [func declineInvite(completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/declineinvite(completionhandler:))
- [func rematch(completionHandler: ((GKTurnBasedMatch?, (any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/rematch(completionhandler:))

### Retrieving Match Details

- [var matchID: String](/documentation/gamekit/gkturnbasedmatch/matchid)
- [var creationDate: Date](/documentation/gamekit/gkturnbasedmatch/creationdate)
- [var participants: [GKTurnBasedParticipant]](/documentation/gamekit/gkturnbasedmatch/participants)
- [var currentParticipant: GKTurnBasedParticipant?](/documentation/gamekit/gkturnbasedmatch/currentparticipant)
- [var status: GKTurnBasedMatch.Status](/documentation/gamekit/gkturnbasedmatch/status-swift.property)
- [GKTurnBasedMatch.Status](/documentation/gamekit/gkturnbasedmatch/status-swift.enum)

#### Match Statuses

- [case unknown](/documentation/gamekit/gkturnbasedmatch/status-swift.enum/unknown)
- [case open](/documentation/gamekit/gkturnbasedmatch/status-swift.enum/open)
- [case ended](/documentation/gamekit/gkturnbasedmatch/status-swift.enum/ended)
- [case matching](/documentation/gamekit/gkturnbasedmatch/status-swift.enum/matching)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkturnbasedmatch/status-swift.enum/init(rawvalue:))
- [var matchData: Data?](/documentation/gamekit/gkturnbasedmatch/matchdata)
- [var matchDataMaximumSize: Int](/documentation/gamekit/gkturnbasedmatch/matchdatamaximumsize)
- [func loadMatchData(completionHandler: ((Data?, (any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/loadmatchdata(completionhandler:))

### Ending Turns and Saving Data

- [func endTurn(withNextParticipants: [GKTurnBasedParticipant], turnTimeout: TimeInterval, match: Data, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/endturn(withnextparticipants:turntimeout:match:completionhandler:))
- [func saveCurrentTurn(withMatch: Data, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/savecurrentturn(withmatch:completionhandler:))
- [Turn Timeouts](/documentation/gamekit/turn-timeouts)

#### Timeouts

- [var GKTurnTimeoutDefault: TimeInterval](/documentation/gamekit/gkturntimeoutdefault)
- [var GKTurnTimeoutNone: TimeInterval](/documentation/gamekit/gkturntimeoutnone)

### Forfeiting a Match

- [func participantQuitInTurn(with: GKTurnBasedMatch.Outcome, nextParticipants: [GKTurnBasedParticipant], turnTimeout: TimeInterval, match: Data, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/participantquitinturn(with:nextparticipants:turntimeout:match:completionhandler:))
- [func participantQuitOutOfTurn(with: GKTurnBasedMatch.Outcome, withCompletionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/participantquitoutofturn(with:withcompletionhandler:))
- [GKTurnBasedMatch.Outcome](/documentation/gamekit/gkturnbasedmatch/outcome)

#### Outcomes

- [case none](/documentation/gamekit/gkturnbasedmatch/outcome/none)
- [case quit](/documentation/gamekit/gkturnbasedmatch/outcome/quit)
- [case won](/documentation/gamekit/gkturnbasedmatch/outcome/won)
- [case lost](/documentation/gamekit/gkturnbasedmatch/outcome/lost)
- [case tied](/documentation/gamekit/gkturnbasedmatch/outcome/tied)
- [case timeExpired](/documentation/gamekit/gkturnbasedmatch/outcome/timeexpired)
- [case first](/documentation/gamekit/gkturnbasedmatch/outcome/first)
- [case second](/documentation/gamekit/gkturnbasedmatch/outcome/second)
- [case third](/documentation/gamekit/gkturnbasedmatch/outcome/third)
- [case fourth](/documentation/gamekit/gkturnbasedmatch/outcome/fourth)
- [case customRange](/documentation/gamekit/gkturnbasedmatch/outcome/customrange)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkturnbasedmatch/outcome/init(rawvalue:))

### Ending a Match

- [func endMatchInTurn(withMatch: Data, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/endmatchinturn(withmatch:completionhandler:))
- [func endMatchInTurn(withMatch: Data, leaderboardScores: [GKLeaderboardScore], achievements: [Any], completionHandler: ((any Error)?) -> Void)](/documentation/gamekit/gkturnbasedmatch/endmatchinturn(withmatch:leaderboardscores:achievements:completionhandler:))

### Sending Messages Between Participants

- [var message: String?](/documentation/gamekit/gkturnbasedmatch/message)
- [func setLocalizableMessageWithKey(String, arguments: [String]?)](/documentation/gamekit/gkturnbasedmatch/setlocalizablemessagewithkey(_:arguments:))
- [func sendReminder(to: [GKTurnBasedParticipant], localizableMessageKey: String, arguments: [String], completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/sendreminder(to:localizablemessagekey:arguments:completionhandler:))

### Exchanging Data Between Participants

- [func sendExchange(to: [GKTurnBasedParticipant], data: Data, localizableMessageKey: String, arguments: [String], timeout: TimeInterval, completionHandler: ((GKTurnBasedExchange?, (any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/sendexchange(to:data:localizablemessagekey:arguments:timeout:completionhandler:))
- [Exchange Timeouts](/documentation/gamekit/exchange-timeouts)

#### Timeouts

- [var GKExchangeTimeoutDefault: TimeInterval](/documentation/gamekit/gkexchangetimeoutdefault)
- [var GKExchangeTimeoutNone: TimeInterval](/documentation/gamekit/gkexchangetimeoutnone)
- [var exchangeDataMaximumSize: Int](/documentation/gamekit/gkturnbasedmatch/exchangedatamaximumsize)
- [var exchangeMaxInitiatedExchangesPerPlayer: Int](/documentation/gamekit/gkturnbasedmatch/exchangemaxinitiatedexchangesperplayer)
- [var activeExchanges: [GKTurnBasedExchange]?](/documentation/gamekit/gkturnbasedmatch/activeexchanges)
- [var completedExchanges: [GKTurnBasedExchange]?](/documentation/gamekit/gkturnbasedmatch/completedexchanges)
- [var exchanges: [GKTurnBasedExchange]?](/documentation/gamekit/gkturnbasedmatch/exchanges)
- [func saveMergedMatch(Data, withResolvedExchanges: [GKTurnBasedExchange], completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/savemergedmatch(_:withresolvedexchanges:completionhandler:))

### Loading Existing Matches

- [class func load(withID: String, withCompletionHandler: ((GKTurnBasedMatch?, (any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/load(withid:withcompletionhandler:))
- [class func loadMatches(completionHandler: (([GKTurnBasedMatch]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/loadmatches(completionhandler:))

### Deleting a Match from Game Center

- [func remove(completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/remove(completionhandler:))

### Deprecated Methods

- [func participantQuitInTurn(with: GKTurnBasedMatch.Outcome, nextParticipant: GKTurnBasedParticipant, match: Data, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/participantquitinturn(with:nextparticipant:match:completionhandler:))
- [func endMatchInTurn(withMatch: Data, scores: [GKScore]?, achievements: [GKAchievement]?, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/endmatchinturn(withmatch:scores:achievements:completionhandler:))
- [func endTurn(withNextParticipant: GKTurnBasedParticipant, match: Data, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedmatch/endturn(withnextparticipant:match:completionhandler:))
- [GKTurnBasedParticipant](/documentation/gamekit/gkturnbasedparticipant)

### Retrieving Participant Details

- [var lastTurnDate: Date?](/documentation/gamekit/gkturnbasedparticipant/lastturndate)
- [var timeoutDate: Date?](/documentation/gamekit/gkturnbasedparticipant/timeoutdate)
- [var player: GKPlayer?](/documentation/gamekit/gkturnbasedparticipant/player)
- [var status: GKTurnBasedParticipant.Status](/documentation/gamekit/gkturnbasedparticipant/status-swift.property)
- [GKTurnBasedParticipant.Status](/documentation/gamekit/gkturnbasedparticipant/status-swift.enum)

#### Constants

- [case unknown](/documentation/gamekit/gkturnbasedparticipant/status-swift.enum/unknown)
- [case invited](/documentation/gamekit/gkturnbasedparticipant/status-swift.enum/invited)
- [case declined](/documentation/gamekit/gkturnbasedparticipant/status-swift.enum/declined)
- [case matching](/documentation/gamekit/gkturnbasedparticipant/status-swift.enum/matching)
- [case active](/documentation/gamekit/gkturnbasedparticipant/status-swift.enum/active)
- [case done](/documentation/gamekit/gkturnbasedparticipant/status-swift.enum/done)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkturnbasedparticipant/status-swift.enum/init(rawvalue:))
- [var playerID: String?](/documentation/gamekit/gkturnbasedparticipant/playerid)

### Setting Participant Outcomes

- [var matchOutcome: GKTurnBasedMatch.Outcome](/documentation/gamekit/gkturnbasedparticipant/matchoutcome)
- [GKTurnBasedMatch.Outcome](/documentation/gamekit/gkturnbasedmatch/outcome)

#### Outcomes

- [case none](/documentation/gamekit/gkturnbasedmatch/outcome/none)
- [case quit](/documentation/gamekit/gkturnbasedmatch/outcome/quit)
- [case won](/documentation/gamekit/gkturnbasedmatch/outcome/won)
- [case lost](/documentation/gamekit/gkturnbasedmatch/outcome/lost)
- [case tied](/documentation/gamekit/gkturnbasedmatch/outcome/tied)
- [case timeExpired](/documentation/gamekit/gkturnbasedmatch/outcome/timeexpired)
- [case first](/documentation/gamekit/gkturnbasedmatch/outcome/first)
- [case second](/documentation/gamekit/gkturnbasedmatch/outcome/second)
- [case third](/documentation/gamekit/gkturnbasedmatch/outcome/third)
- [case fourth](/documentation/gamekit/gkturnbasedmatch/outcome/fourth)
- [case customRange](/documentation/gamekit/gkturnbasedmatch/outcome/customrange)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkturnbasedmatch/outcome/init(rawvalue:))
- [GKTurnBasedEventListener](/documentation/gamekit/gkturnbasedeventlistener)

### Handling Match-Related Events

- [func player(GKPlayer, receivedTurnEventFor: GKTurnBasedMatch, didBecomeActive: Bool)](/documentation/gamekit/gkturnbasedeventlistener/player(_:receivedturneventfor:didbecomeactive:))
- [func player(GKPlayer, didRequestMatchWithOtherPlayers: [GKPlayer])](/documentation/gamekit/gkturnbasedeventlistener/player(_:didrequestmatchwithotherplayers:))
- [func player(GKPlayer, matchEnded: GKTurnBasedMatch)](/documentation/gamekit/gkturnbasedeventlistener/player(_:matchended:))
- [func player(GKPlayer, wantsToQuitMatch: GKTurnBasedMatch)](/documentation/gamekit/gkturnbasedeventlistener/player(_:wantstoquitmatch:))
- [func player(GKPlayer, didRequestMatchWithPlayers: [String])](/documentation/gamekit/gkturnbasedeventlistener/player(_:didrequestmatchwithplayers:))

### Handling Data Exchanges

- [func player(GKPlayer, receivedExchangeRequest: GKTurnBasedExchange, for: GKTurnBasedMatch)](/documentation/gamekit/gkturnbasedeventlistener/player(_:receivedexchangerequest:for:))
- [func player(GKPlayer, receivedExchangeReplies: [GKTurnBasedExchangeReply], forCompletedExchange: GKTurnBasedExchange, for: GKTurnBasedMatch)](/documentation/gamekit/gkturnbasedeventlistener/player(_:receivedexchangereplies:forcompletedexchange:for:))
- [func player(GKPlayer, receivedExchangeCancellation: GKTurnBasedExchange, for: GKTurnBasedMatch)](/documentation/gamekit/gkturnbasedeventlistener/player(_:receivedexchangecancellation:for:))
- [GKTurnBasedExchange](/documentation/gamekit/gkturnbasedexchange)

### Retrieving Exchange Details

- [var exchangeID: String](/documentation/gamekit/gkturnbasedexchange/exchangeid)
- [var sender: GKTurnBasedParticipant](/documentation/gamekit/gkturnbasedexchange/sender)
- [var recipients: [GKTurnBasedParticipant]](/documentation/gamekit/gkturnbasedexchange/recipients)
- [var data: Data?](/documentation/gamekit/gkturnbasedexchange/data)
- [var message: String?](/documentation/gamekit/gkturnbasedexchange/message)
- [var sendDate: Date](/documentation/gamekit/gkturnbasedexchange/senddate)
- [var timeoutDate: Date?](/documentation/gamekit/gkturnbasedexchange/timeoutdate)

### Replying to Exchange Requests

- [func reply(withLocalizableMessageKey: String, arguments: [String], data: Data, completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedexchange/reply(withlocalizablemessagekey:arguments:data:completionhandler:))
- [var replies: [GKTurnBasedExchangeReply]?](/documentation/gamekit/gkturnbasedexchange/replies)
- [var status: GKTurnBasedExchangeStatus](/documentation/gamekit/gkturnbasedexchange/status)
- [GKTurnBasedExchangeStatus](/documentation/gamekit/gkturnbasedexchangestatus)

#### Statuses

- [case unknown](/documentation/gamekit/gkturnbasedexchangestatus/unknown)
- [case active](/documentation/gamekit/gkturnbasedexchangestatus/active)
- [case complete](/documentation/gamekit/gkturnbasedexchangestatus/complete)
- [case resolved](/documentation/gamekit/gkturnbasedexchangestatus/resolved)
- [case canceled](/documentation/gamekit/gkturnbasedexchangestatus/canceled)

#### Initializers

- [init?(rawValue: Int8)](/documentation/gamekit/gkturnbasedexchangestatus/init(rawvalue:))
- [var completionDate: Date?](/documentation/gamekit/gkturnbasedexchange/completiondate)

### Canceling Exchange Requests

- [func cancel(withLocalizableMessageKey: String, arguments: [String], completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkturnbasedexchange/cancel(withlocalizablemessagekey:arguments:completionhandler:))
- [GKTurnBasedExchangeReply](/documentation/gamekit/gkturnbasedexchangereply)

### Retrieving Reply Details

- [var data: Data?](/documentation/gamekit/gkturnbasedexchangereply/data)
- [var message: String?](/documentation/gamekit/gkturnbasedexchangereply/message)
- [var recipient: GKTurnBasedParticipant](/documentation/gamekit/gkturnbasedexchangereply/recipient)
- [var replyDate: Date](/documentation/gamekit/gkturnbasedexchangereply/replydate)
- [GKGameCenterBadgingDisabled](/documentation/bundleresources/information-property-list/gkgamecenterbadgingdisabled)

## Errors

- [GKError](/documentation/gamekit/gkerror)

### Error Codes

- [GKError.Code](/documentation/gamekit/gkerror/code)

#### Configuration Errors

- [case gameUnrecognized](/documentation/gamekit/gkerror/code/gameunrecognized)
- [case notSupported](/documentation/gamekit/gkerror/code/notsupported)
- [case appUnlisted](/documentation/gamekit/gkerror/code/appunlisted)

#### Communication Errors

- [case unknown](/documentation/gamekit/gkerror/code/unknown)
- [case cancelled](/documentation/gamekit/gkerror/code/cancelled)
- [case communicationsFailure](/documentation/gamekit/gkerror/code/communicationsfailure)
- [case invalidPlayer](/documentation/gamekit/gkerror/code/invalidplayer)
- [case invalidParameter](/documentation/gamekit/gkerror/code/invalidparameter)
- [case gameSessionRequestInvalid](/documentation/gamekit/gkerror/code/gamesessionrequestinvalid)
- [case apiNotAvailable](/documentation/gamekit/gkerror/code/apinotavailable)
- [case connectionTimeout](/documentation/gamekit/gkerror/code/connectiontimeout)
- [case apiObsolete](/documentation/gamekit/gkerror/code/apiobsolete)

#### Player-Related Errors

- [case userDenied](/documentation/gamekit/gkerror/code/userdenied)
- [case invalidCredentials](/documentation/gamekit/gkerror/code/invalidcredentials)
- [case notAuthenticated](/documentation/gamekit/gkerror/code/notauthenticated)
- [case authenticationInProgress](/documentation/gamekit/gkerror/code/authenticationinprogress)
- [case parentalControlsBlocked](/documentation/gamekit/gkerror/code/parentalcontrolsblocked)
- [case playerStatusExceedsMaximumLength](/documentation/gamekit/gkerror/code/playerstatusexceedsmaximumlength)
- [case playerStatusInvalid](/documentation/gamekit/gkerror/code/playerstatusinvalid)
- [case underage](/documentation/gamekit/gkerror/code/underage)
- [case playerPhotoFailure](/documentation/gamekit/gkerror/code/playerphotofailure)
- [case ubiquityContainerUnavailable](/documentation/gamekit/gkerror/code/ubiquitycontainerunavailable)
- [case notAuthorized](/documentation/gamekit/gkerror/code/notauthorized)
- [case iCloudUnavailable](/documentation/gamekit/gkerror/code/icloudunavailable)
- [case lockdownMode](/documentation/gamekit/gkerror/code/lockdownmode)

#### Friend List Errors

- [case friendListDescriptionMissing](/documentation/gamekit/gkerror/code/friendlistdescriptionmissing)
- [case friendListRestricted](/documentation/gamekit/gkerror/code/friendlistrestricted)
- [case friendListDenied](/documentation/gamekit/gkerror/code/friendlistdenied)
- [case friendRequestNotAvailable](/documentation/gamekit/gkerror/code/friendrequestnotavailable)

#### Matchmaking Errors

- [case matchRequestInvalid](/documentation/gamekit/gkerror/code/matchrequestinvalid)
- [case unexpectedConnection](/documentation/gamekit/gkerror/code/unexpectedconnection)
- [case invitationsDisabled](/documentation/gamekit/gkerror/code/invitationsdisabled)
- [case matchNotConnected](/documentation/gamekit/gkerror/code/matchnotconnected)
- [case restrictedToAutomatch](/documentation/gamekit/gkerror/code/restrictedtoautomatch)

#### Turn-Based Game Errors

- [case turnBasedMatchDataTooLarge](/documentation/gamekit/gkerror/code/turnbasedmatchdatatoolarge)
- [case turnBasedTooManySessions](/documentation/gamekit/gkerror/code/turnbasedtoomanysessions)
- [case turnBasedInvalidParticipant](/documentation/gamekit/gkerror/code/turnbasedinvalidparticipant)
- [case turnBasedInvalidTurn](/documentation/gamekit/gkerror/code/turnbasedinvalidturn)
- [case turnBasedInvalidState](/documentation/gamekit/gkerror/code/turnbasedinvalidstate)

#### Leaderboard Errors

- [case scoreNotSet](/documentation/gamekit/gkerror/code/scorenotset)

#### Challenges Errors

- [case challengeInvalid](/documentation/gamekit/gkerror/code/challengeinvalid)

#### Enumeration Cases

- [case debugMode](/documentation/gamekit/gkerror/code/debugmode)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkerror/code/init(rawvalue:))
- [static var authenticationInProgress: GKError.Code](/documentation/gamekit/gkerror/authenticationinprogress)
- [static var cancelled: GKError.Code](/documentation/gamekit/gkerror/cancelled)
- [static var challengeInvalid: GKError.Code](/documentation/gamekit/gkerror/challengeinvalid)
- [static var communicationsFailure: GKError.Code](/documentation/gamekit/gkerror/communicationsfailure)
- [static var gameSessionRequestInvalid: GKError.Code](/documentation/gamekit/gkerror/gamesessionrequestinvalid)
- [static var gameUnrecognized: GKError.Code](/documentation/gamekit/gkerror/gameunrecognized)
- [static var invalidCredentials: GKError.Code](/documentation/gamekit/gkerror/invalidcredentials)
- [static var invalidParameter: GKError.Code](/documentation/gamekit/gkerror/invalidparameter)
- [static var invalidPlayer: GKError.Code](/documentation/gamekit/gkerror/invalidplayer)
- [static var invitationsDisabled: GKError.Code](/documentation/gamekit/gkerror/invitationsdisabled)
- [static var matchNotConnected: GKError.Code](/documentation/gamekit/gkerror/matchnotconnected)
- [static var matchRequestInvalid: GKError.Code](/documentation/gamekit/gkerror/matchrequestinvalid)
- [static var notAuthenticated: GKError.Code](/documentation/gamekit/gkerror/notauthenticated)
- [static var notSupported: GKError.Code](/documentation/gamekit/gkerror/notsupported)
- [static var parentalControlsBlocked: GKError.Code](/documentation/gamekit/gkerror/parentalcontrolsblocked)
- [static var playerPhotoFailure: GKError.Code](/documentation/gamekit/gkerror/playerphotofailure)
- [static var playerStatusExceedsMaximumLength: GKError.Code](/documentation/gamekit/gkerror/playerstatusexceedsmaximumlength)
- [static var playerStatusInvalid: GKError.Code](/documentation/gamekit/gkerror/playerstatusinvalid)
- [static var scoreNotSet: GKError.Code](/documentation/gamekit/gkerror/scorenotset)
- [static var turnBasedInvalidParticipant: GKError.Code](/documentation/gamekit/gkerror/turnbasedinvalidparticipant)
- [static var turnBasedInvalidState: GKError.Code](/documentation/gamekit/gkerror/turnbasedinvalidstate)
- [static var turnBasedInvalidTurn: GKError.Code](/documentation/gamekit/gkerror/turnbasedinvalidturn)
- [static var turnBasedMatchDataTooLarge: GKError.Code](/documentation/gamekit/gkerror/turnbasedmatchdatatoolarge)
- [static var turnBasedTooManySessions: GKError.Code](/documentation/gamekit/gkerror/turnbasedtoomanysessions)
- [static var ubiquityContainerUnavailable: GKError.Code](/documentation/gamekit/gkerror/ubiquitycontainerunavailable)
- [static var underage: GKError.Code](/documentation/gamekit/gkerror/underage)
- [static var unexpectedConnection: GKError.Code](/documentation/gamekit/gkerror/unexpectedconnection)
- [static var unknown: GKError.Code](/documentation/gamekit/gkerror/unknown)
- [static var userDenied: GKError.Code](/documentation/gamekit/gkerror/userdenied)
- [static var restrictedToAutomatch: GKError.Code](/documentation/gamekit/gkerror/restrictedtoautomatch)
- [static var apiNotAvailable: GKError.Code](/documentation/gamekit/gkerror/apinotavailable)
- [static var notAuthorized: GKError.Code](/documentation/gamekit/gkerror/notauthorized)
- [static var connectionTimeout: GKError.Code](/documentation/gamekit/gkerror/connectiontimeout)
- [static var apiObsolete: GKError.Code](/documentation/gamekit/gkerror/apiobsolete)
- [static var iCloudUnavailable: GKError.Code](/documentation/gamekit/gkerror/icloudunavailable)
- [static var lockdownMode: GKError.Code](/documentation/gamekit/gkerror/lockdownmode)
- [static var appUnlisted: GKError.Code](/documentation/gamekit/gkerror/appunlisted)
- [static var friendListDescriptionMissing: GKError.Code](/documentation/gamekit/gkerror/friendlistdescriptionmissing)
- [static var friendListRestricted: GKError.Code](/documentation/gamekit/gkerror/friendlistrestricted)
- [static var friendListDenied: GKError.Code](/documentation/gamekit/gkerror/friendlistdenied)
- [static var friendRequestNotAvailable: GKError.Code](/documentation/gamekit/gkerror/friendrequestnotavailable)

### Error Domain

- [static var errorDomain: String](/documentation/gamekit/gkerror/errordomain)

### Type Properties

- [static var debugMode: GKError.Code](/documentation/gamekit/gkerror/debugmode)
- [GKError.Code](/documentation/gamekit/gkerror/code)

### Configuration Errors

- [case gameUnrecognized](/documentation/gamekit/gkerror/code/gameunrecognized)
- [case notSupported](/documentation/gamekit/gkerror/code/notsupported)
- [case appUnlisted](/documentation/gamekit/gkerror/code/appunlisted)

### Communication Errors

- [case unknown](/documentation/gamekit/gkerror/code/unknown)
- [case cancelled](/documentation/gamekit/gkerror/code/cancelled)
- [case communicationsFailure](/documentation/gamekit/gkerror/code/communicationsfailure)
- [case invalidPlayer](/documentation/gamekit/gkerror/code/invalidplayer)
- [case invalidParameter](/documentation/gamekit/gkerror/code/invalidparameter)
- [case gameSessionRequestInvalid](/documentation/gamekit/gkerror/code/gamesessionrequestinvalid)
- [case apiNotAvailable](/documentation/gamekit/gkerror/code/apinotavailable)
- [case connectionTimeout](/documentation/gamekit/gkerror/code/connectiontimeout)
- [case apiObsolete](/documentation/gamekit/gkerror/code/apiobsolete)

### Player-Related Errors

- [case userDenied](/documentation/gamekit/gkerror/code/userdenied)
- [case invalidCredentials](/documentation/gamekit/gkerror/code/invalidcredentials)
- [case notAuthenticated](/documentation/gamekit/gkerror/code/notauthenticated)
- [case authenticationInProgress](/documentation/gamekit/gkerror/code/authenticationinprogress)
- [case parentalControlsBlocked](/documentation/gamekit/gkerror/code/parentalcontrolsblocked)
- [case playerStatusExceedsMaximumLength](/documentation/gamekit/gkerror/code/playerstatusexceedsmaximumlength)
- [case playerStatusInvalid](/documentation/gamekit/gkerror/code/playerstatusinvalid)
- [case underage](/documentation/gamekit/gkerror/code/underage)
- [case playerPhotoFailure](/documentation/gamekit/gkerror/code/playerphotofailure)
- [case ubiquityContainerUnavailable](/documentation/gamekit/gkerror/code/ubiquitycontainerunavailable)
- [case notAuthorized](/documentation/gamekit/gkerror/code/notauthorized)
- [case iCloudUnavailable](/documentation/gamekit/gkerror/code/icloudunavailable)
- [case lockdownMode](/documentation/gamekit/gkerror/code/lockdownmode)

### Friend List Errors

- [case friendListDescriptionMissing](/documentation/gamekit/gkerror/code/friendlistdescriptionmissing)
- [case friendListRestricted](/documentation/gamekit/gkerror/code/friendlistrestricted)
- [case friendListDenied](/documentation/gamekit/gkerror/code/friendlistdenied)
- [case friendRequestNotAvailable](/documentation/gamekit/gkerror/code/friendrequestnotavailable)

### Matchmaking Errors

- [case matchRequestInvalid](/documentation/gamekit/gkerror/code/matchrequestinvalid)
- [case unexpectedConnection](/documentation/gamekit/gkerror/code/unexpectedconnection)
- [case invitationsDisabled](/documentation/gamekit/gkerror/code/invitationsdisabled)
- [case matchNotConnected](/documentation/gamekit/gkerror/code/matchnotconnected)
- [case restrictedToAutomatch](/documentation/gamekit/gkerror/code/restrictedtoautomatch)

### Turn-Based Game Errors

- [case turnBasedMatchDataTooLarge](/documentation/gamekit/gkerror/code/turnbasedmatchdatatoolarge)
- [case turnBasedTooManySessions](/documentation/gamekit/gkerror/code/turnbasedtoomanysessions)
- [case turnBasedInvalidParticipant](/documentation/gamekit/gkerror/code/turnbasedinvalidparticipant)
- [case turnBasedInvalidTurn](/documentation/gamekit/gkerror/code/turnbasedinvalidturn)
- [case turnBasedInvalidState](/documentation/gamekit/gkerror/code/turnbasedinvalidstate)

### Leaderboard Errors

- [case scoreNotSet](/documentation/gamekit/gkerror/code/scorenotset)

### Challenges Errors

- [case challengeInvalid](/documentation/gamekit/gkerror/code/challengeinvalid)

### Enumeration Cases

- [case debugMode](/documentation/gamekit/gkerror/code/debugmode)

### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkerror/code/init(rawvalue:))
- [let GKErrorDomain: String](/documentation/gamekit/gkerrordomain)

## Deprecated

- [Deprecated symbols](/documentation/gamekit/deprecated-symbols)

### Deprecated classes

- [GKAchievementViewController](/documentation/gamekit/gkachievementviewcontroller)

#### Setting the Delegate

- [var achievementDelegate: (any GKAchievementViewControllerDelegate)!](/documentation/gamekit/gkachievementviewcontroller/achievementdelegate)
- [GKChallengeEventHandler](/documentation/gamekit/gkchallengeeventhandler)

#### Getting and Setting the Delegate

- [var delegate: (any GKChallengeEventHandlerDelegate)!](/documentation/gamekit/gkchallengeeventhandler/delegate)
- [GKChallengesViewController](/documentation/gamekit/gkchallengesviewcontroller)

#### Getting the Delegate

- [var challengeDelegate: (any GKChallengesViewControllerDelegate)!](/documentation/gamekit/gkchallengesviewcontroller/challengedelegate)
- [GKChallenge](/documentation/gamekit/gkchallenge)

#### Retrieving the List of Challenges to the Local Player

- [class func loadReceivedChallenges(completionHandler: (([GKChallenge]?, (any Error)?) -> Void)?)](/documentation/gamekit/gkchallenge/loadreceivedchallenges(completionhandler:))

#### Examining Details about a Challenge

- [var issuingPlayer: GKPlayer?](/documentation/gamekit/gkchallenge/issuingplayer)
- [var receivingPlayer: GKPlayer?](/documentation/gamekit/gkchallenge/receivingplayer)
- [var message: String?](/documentation/gamekit/gkchallenge/message)
- [var state: GKChallengeState](/documentation/gamekit/gkchallenge/state)
- [GKChallengeState](/documentation/gamekit/gkchallengestate)

##### Challenge States

- [case invalid](/documentation/gamekit/gkchallengestate/invalid)
- [case pending](/documentation/gamekit/gkchallengestate/pending)
- [case completed](/documentation/gamekit/gkchallengestate/completed)
- [case declined](/documentation/gamekit/gkchallengestate/declined)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkchallengestate/init(rawvalue:))
- [var issueDate: Date](/documentation/gamekit/gkchallenge/issuedate)
- [var completionDate: Date?](/documentation/gamekit/gkchallenge/completiondate)

#### Declining a Challenge

- [func decline()](/documentation/gamekit/gkchallenge/decline())

#### Deprecated symbols

- [var issuingPlayerID: String?](/documentation/gamekit/gkchallenge/issuingplayerid)
- [var receivingPlayerID: String?](/documentation/gamekit/gkchallenge/receivingplayerid)
- [GKChallengeComposeCompletionBlock](/documentation/gamekit/gkchallengecomposecompletionblock)
- [GKScoreChallenge](/documentation/gamekit/gkscorechallenge)

#### Obtaining the score to beat

- [var leaderboardEntry: GKLeaderboard.Entry?](/documentation/gamekit/gkscorechallenge/leaderboardentry)
- [var score: GKScore?](/documentation/gamekit/gkscorechallenge/score)
- [GKAchievementChallenge](/documentation/gamekit/gkachievementchallenge)

#### Obtaining the Achievement

- [var achievement: GKAchievement?](/documentation/gamekit/gkachievementchallenge/achievement)
- [GKCloudPlayer](/documentation/gamekit/gkcloudplayer)

#### Retrieving Information About a Signed-in Player

- [class func getCurrentSignedInPlayer(forContainer: String?, completionHandler: (GKCloudPlayer?, (any Error)?) -> Void)](/documentation/gamekit/gkcloudplayer/getcurrentsignedinplayer(forcontainer:completionhandler:))
- [GKGameCenterViewController](/documentation/gamekit/gkgamecenterviewcontroller)

#### Configuring Game Center content

- [init(state: GKGameCenterViewControllerState)](/documentation/gamekit/gkgamecenterviewcontroller/init(state:))
- [GKGameCenterViewControllerState](/documentation/gamekit/gkgamecenterviewcontrollerstate)

##### States

- [case `default`](/documentation/gamekit/gkgamecenterviewcontrollerstate/default)
- [case leaderboards](/documentation/gamekit/gkgamecenterviewcontrollerstate/leaderboards)
- [case achievements](/documentation/gamekit/gkgamecenterviewcontrollerstate/achievements)
- [case challenges](/documentation/gamekit/gkgamecenterviewcontrollerstate/challenges)
- [case localPlayerProfile](/documentation/gamekit/gkgamecenterviewcontrollerstate/localplayerprofile)
- [case dashboard](/documentation/gamekit/gkgamecenterviewcontrollerstate/dashboard)
- [case localPlayerFriendsList](/documentation/gamekit/gkgamecenterviewcontrollerstate/localplayerfriendslist)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkgamecenterviewcontrollerstate/init(rawvalue:))
- [init(leaderboard: GKLeaderboard, playerScope: GKLeaderboard.PlayerScope)](/documentation/gamekit/gkgamecenterviewcontroller/init(leaderboard:playerscope:))
- [init(leaderboardID: String, playerScope: GKLeaderboard.PlayerScope, timeScope: GKLeaderboard.TimeScope)](/documentation/gamekit/gkgamecenterviewcontroller/init(leaderboardid:playerscope:timescope:))
- [init(leaderboardSetID: String)](/documentation/gamekit/gkgamecenterviewcontroller/init(leaderboardsetid:))
- [init(achievementID: String)](/documentation/gamekit/gkgamecenterviewcontroller/init(achievementid:))
- [init(player: GKPlayer)](/documentation/gamekit/gkgamecenterviewcontroller/init(player:))

#### Setting the view controller delegate

- [var gameCenterDelegate: (any GKGameCenterControllerDelegate)?](/documentation/gamekit/gkgamecenterviewcontroller/gamecenterdelegate)
- [GKGameCenterControllerDelegate](/documentation/gamekit/gkgamecentercontrollerdelegate)

##### Handling User Actions

- [func gameCenterViewControllerDidFinish(GKGameCenterViewController)](/documentation/gamekit/gkgamecentercontrollerdelegate/gamecenterviewcontrollerdidfinish(_:))

#### Deprecated

- [Deprecated Symbols](/documentation/gamekit/gkgamecenterviewcontroller-deprecated-symbols)

##### Deprecated Properties

- [var viewState: GKGameCenterViewControllerState](/documentation/gamekit/gkgamecenterviewcontroller/viewstate)
- [var leaderboardIdentifier: String?](/documentation/gamekit/gkgamecenterviewcontroller/leaderboardidentifier)
- [var leaderboardCategory: String?](/documentation/gamekit/gkgamecenterviewcontroller/leaderboardcategory)
- [var leaderboardTimeScope: GKLeaderboard.TimeScope](/documentation/gamekit/gkgamecenterviewcontroller/leaderboardtimescope)
- [GKGameSession](/documentation/gamekit/gkgamesession)

#### Creating and Loading Game Sessions

- [class func createSession(inContainer: String?, withTitle: String, maxConnectedPlayers: Int, completionHandler: (GKGameSession?, (any Error)?) -> Void)](/documentation/gamekit/gkgamesession/createsession(incontainer:withtitle:maxconnectedplayers:completionhandler:))
- [class func load(withIdentifier: String, completionHandler: (GKGameSession?, (any Error)?) -> Void)](/documentation/gamekit/gkgamesession/load(withidentifier:completionhandler:))
- [class func loadSessions(inContainer: String?, completionHandler: ([GKGameSession]?, (any Error)?) -> Void)](/documentation/gamekit/gkgamesession/loadsessions(incontainer:completionhandler:))
- [class func remove(withIdentifier: String, completionHandler: ((any Error)?) -> Void)](/documentation/gamekit/gkgamesession/remove(withidentifier:completionhandler:))

#### Accessing Information About a Game Session

- [var identifier: String](/documentation/gamekit/gkgamesession/identifier)
- [var lastModifiedDate: Date](/documentation/gamekit/gkgamesession/lastmodifieddate)
- [var lastModifiedPlayer: GKCloudPlayer](/documentation/gamekit/gkgamesession/lastmodifiedplayer)
- [var maxNumberOfConnectedPlayers: Int](/documentation/gamekit/gkgamesession/maxnumberofconnectedplayers)
- [var owner: GKCloudPlayer](/documentation/gamekit/gkgamesession/owner)
- [var players: [GKCloudPlayer]](/documentation/gamekit/gkgamesession/players)
- [var title: String](/documentation/gamekit/gkgamesession/title)

#### Inviting Players to a Game Session

- [func getShareURL(completionHandler: (URL?, (any Error)?) -> Void)](/documentation/gamekit/gkgamesession/getshareurl(completionhandler:))

#### Saving and Loading Data

- [func loadData(completionHandler: (Data?, (any Error)?) -> Void)](/documentation/gamekit/gkgamesession/loaddata(completionhandler:))
- [func save(Data, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/gamekit/gkgamesession/save(_:completionhandler:))

#### Listening for Events

- [class func add(listener: any GKGameSessionEventListener)](/documentation/gamekit/gkgamesession/add(listener:))
- [class func remove(listener: any GKGameSessionEventListener)](/documentation/gamekit/gkgamesession/remove(listener:))

#### Connecting Players for Real-Time Communication

- [func setConnectionState(GKConnectionState, completionHandler: ((any Error)?) -> Void)](/documentation/gamekit/gkgamesession/setconnectionstate(_:completionhandler:))
- [func players(with: GKConnectionState) -> [GKCloudPlayer]](/documentation/gamekit/gkgamesession/players(with:))
- [func send(Data, with: GKTransportType, completionHandler: ((any Error)?) -> Void)](/documentation/gamekit/gkgamesession/send(_:with:completionhandler:))
- [GKTransportType](/documentation/gamekit/gktransporttype)

##### Constants

- [case reliable](/documentation/gamekit/gktransporttype/reliable)
- [case unreliable](/documentation/gamekit/gktransporttype/unreliable)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gktransporttype/init(rawvalue:))

#### Communicating Between Players

- [var badgedPlayers: [GKCloudPlayer]](/documentation/gamekit/gkgamesession/badgedplayers)
- [func clearBadge(for: [GKCloudPlayer], completionHandler: ((any Error)?) -> Void)](/documentation/gamekit/gkgamesession/clearbadge(for:completionhandler:))
- [func sendMessage(withLocalizedFormatKey: String, arguments: [String], data: Data?, to: [GKCloudPlayer], badgePlayers: Bool, completionHandler: ((any Error)?) -> Void)](/documentation/gamekit/gkgamesession/sendmessage(withlocalizedformatkey:arguments:data:to:badgeplayers:completionhandler:))
- [GKGameSessionSharingViewController](/documentation/gamekit/gkgamesessionsharingviewcontroller)

#### Presenting the Share UI

- [init(session: GKGameSession)](/documentation/gamekit/gkgamesessionsharingviewcontroller/init(session:))

#### Accessing Share View Controller Properties

- [var delegate: (any GKGameSessionSharingViewControllerDelegate)?](/documentation/gamekit/gkgamesessionsharingviewcontroller/delegate)
- [GKGameSessionSharingViewControllerDelegate](/documentation/gamekit/gkgamesessionsharingviewcontrollerdelegate)

##### Dismissing a Sharing View Controller

- [func sharingViewController(GKGameSessionSharingViewController, didFinishWithError: (any Error)?)](/documentation/gamekit/gkgamesessionsharingviewcontrollerdelegate/sharingviewcontroller(_:didfinishwitherror:))
- [var session: GKGameSession](/documentation/gamekit/gkgamesessionsharingviewcontroller/session)
- [GKFriendRequestComposeViewController](/documentation/gamekit/gkfriendrequestcomposeviewcontroller)

#### Determining the Maximum Number of Recipients

- [class func maxNumberOfRecipients() -> Int](/documentation/gamekit/gkfriendrequestcomposeviewcontroller/maxnumberofrecipients())

#### Delegate

- [var composeViewDelegate: (any GKFriendRequestComposeViewControllerDelegate)?](/documentation/gamekit/gkfriendrequestcomposeviewcontroller/composeviewdelegate)

#### Adding Recipients

- [func addRecipients(withEmailAddresses: [String])](/documentation/gamekit/gkfriendrequestcomposeviewcontroller/addrecipients(withemailaddresses:))
- [func addRecipientPlayers([GKPlayer])](/documentation/gamekit/gkfriendrequestcomposeviewcontroller/addrecipientplayers(_:))
- [func addRecipients(withPlayerIDs: [String])](/documentation/gamekit/gkfriendrequestcomposeviewcontroller/addrecipients(withplayerids:))

#### Setting an Invitation Message

- [func setMessage(String?)](/documentation/gamekit/gkfriendrequestcomposeviewcontroller/setmessage(_:))
- [GKLeaderboardViewController](/documentation/gamekit/gkleaderboardviewcontroller)

#### Configuring the Leaderboard View Controller

- [var category: String!](/documentation/gamekit/gkleaderboardviewcontroller/category)
- [var leaderboardDelegate: (any GKLeaderboardViewControllerDelegate)!](/documentation/gamekit/gkleaderboardviewcontroller/leaderboarddelegate)
- [var timeScope: GKLeaderboard.TimeScope](/documentation/gamekit/gkleaderboardviewcontroller/timescope)
- [GKPeerPickerController](/documentation/gamekit/gkpeerpickercontroller)

#### Setting and Getting the Delegate

- [var delegate: (any GKPeerPickerControllerDelegate)?](/documentation/gamekit/gkpeerpickercontroller/delegate)

#### Displaying the Picker Dialog

- [func dismiss()](/documentation/gamekit/gkpeerpickercontroller/dismiss())
- [func show()](/documentation/gamekit/gkpeerpickercontroller/show())
- [var isVisible: Bool](/documentation/gamekit/gkpeerpickercontroller/isvisible)

#### Configuring Connectivity Options

- [var connectionTypesMask: GKPeerPickerConnectionType](/documentation/gamekit/gkpeerpickercontroller/connectiontypesmask)

#### Constants

- [GKPeerPickerConnectionType](/documentation/gamekit/gkpeerpickerconnectiontype)

##### Constants

- [case nearby](/documentation/gamekit/gkpeerpickerconnectiontype/nearby)
- [case online](/documentation/gamekit/gkpeerpickerconnectiontype/online)
- [case nearby](/documentation/gamekit/gkpeerpickerconnectiontype/nearby)

##### Initializers

- [init?(rawValue: UInt)](/documentation/gamekit/gkpeerpickerconnectiontype/init(rawvalue:))
- [GKScore](/documentation/gamekit/gkscore)

#### Reporting a New Score

- [class func report([GKLeaderboardScore], withEligibleChallenges: [GKChallenge], withCompletionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkscore/report(_:witheligiblechallenges:withcompletionhandler:)-2tycl)
- [class func report([GKScore], withCompletionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkscore/report(_:withcompletionhandler:))
- [class func report([GKScore], withEligibleChallenges: [GKChallenge], withCompletionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkscore/report(_:witheligiblechallenges:withcompletionhandler:)-3c5lh)

#### Issuing a Score Challenge

- [func challengeComposeController(withMessage: String?, players: [GKPlayer]?, completion: GKChallengeComposeHandler?) -> UIViewController](/documentation/gamekit/gkscore/challengecomposecontroller(withmessage:players:completion:))
- [GKChallengeComposeHandler](/documentation/gamekit/gkchallengecomposehandler)
- [func challengeComposeController(withMessage: String?, players: [GKPlayer]?, completionHandler: GKChallengeComposeCompletionBlock?) -> UIViewController](/documentation/gamekit/gkscore/challengecomposecontroller(withmessage:players:completionhandler:))
- [func challengeComposeController(withPlayers: [String]?, message: String?, completionHandler: GKChallengeComposeCompletionBlock?) -> UIViewController?](/documentation/gamekit/gkscore/challengecomposecontroller(withplayers:message:completionhandler:))

#### Deprecated Methods and Properties

- [var category: String?](/documentation/gamekit/gkscore/category)
- [var context: UInt64](/documentation/gamekit/gkscore/context)
- [var date: Date](/documentation/gamekit/gkscore/date)
- [var formattedValue: String?](/documentation/gamekit/gkscore/formattedvalue)
- [var leaderboardIdentifier: String](/documentation/gamekit/gkscore/leaderboardidentifier)
- [var player: GKPlayer](/documentation/gamekit/gkscore/player)
- [var rank: Int](/documentation/gamekit/gkscore/rank)
- [var value: Int64](/documentation/gamekit/gkscore/value)
- [var shouldSetDefaultLeaderboard: Bool](/documentation/gamekit/gkscore/shouldsetdefaultleaderboard)
- [init(leaderboardIdentifier: String)](/documentation/gamekit/gkscore/init(leaderboardidentifier:))
- [init(leaderboardIdentifier: String, player: GKPlayer)](/documentation/gamekit/gkscore/init(leaderboardidentifier:player:))
- [init(category: String?)](/documentation/gamekit/gkscore/init(category:))
- [init?(leaderboardIdentifier: String, forPlayer: String)](/documentation/gamekit/gkscore/init(leaderboardidentifier:forplayer:))
- [func issueChallenge(toPlayers: [String]?, message: String?)](/documentation/gamekit/gkscore/issuechallenge(toplayers:message:))
- [var playerID: String?](/documentation/gamekit/gkscore/playerid)
- [func report(completionHandler: (((any Error)?) -> Void)?)](/documentation/gamekit/gkscore/report(completionhandler:))
- [GKSession](/documentation/gamekit/gksession)

#### Creating a Session

- [init!(sessionID: String!, displayName: String!, sessionMode: GKSessionMode)](/documentation/gamekit/gksession/init(sessionid:displayname:sessionmode:))

#### Setting and Getting the Delegate

- [var delegate: (any GKSessionDelegate)!](/documentation/gamekit/gksession/delegate)

#### Searching for Other Peers

- [var isAvailable: Bool](/documentation/gamekit/gksession/isavailable)

#### Obtaining Information About Other Peers

- [func peers(with: GKPeerConnectionState) -> [Any]!](/documentation/gamekit/gksession/peers(with:))
- [func displayName(forPeer: String!) -> String!](/documentation/gamekit/gksession/displayname(forpeer:))

#### Connecting to a Remote Peer

- [func connect(toPeer: String!, withTimeout: TimeInterval)](/documentation/gamekit/gksession/connect(topeer:withtimeout:))
- [func cancelConnect(toPeer: String!)](/documentation/gamekit/gksession/cancelconnect(topeer:))

#### Receiving Connections from a Remote Peer

- [func acceptConnection(fromPeer: String!) throws](/documentation/gamekit/gksession/acceptconnection(frompeer:))
- [func denyConnection(fromPeer: String!)](/documentation/gamekit/gksession/denyconnection(frompeer:))

#### Working with Connected Peers

- [func setDataReceiveHandler(Any!, withContext: UnsafeMutableRawPointer!)](/documentation/gamekit/gksession/setdatareceivehandler(_:withcontext:))
- [func send(Data!, toPeers: [Any]!, with: GKSendDataMode) throws](/documentation/gamekit/gksession/send(_:topeers:with:))
- [func sendData(toAllPeers: Data!, with: GKSendDataMode) throws](/documentation/gamekit/gksession/senddata(toallpeers:with:))
- [var disconnectTimeout: TimeInterval](/documentation/gamekit/gksession/disconnecttimeout)
- [func disconnectFromAllPeers()](/documentation/gamekit/gksession/disconnectfromallpeers())
- [func disconnectPeer(fromAllPeers: String!)](/documentation/gamekit/gksession/disconnectpeer(fromallpeers:))

#### Information about the Session

- [var displayName: String!](/documentation/gamekit/gksession/displayname)
- [var peerID: String!](/documentation/gamekit/gksession/peerid)
- [var sessionID: String!](/documentation/gamekit/gksession/sessionid)
- [var sessionMode: GKSessionMode](/documentation/gamekit/gksession/sessionmode)

#### Constants

- [GKSendDataMode](/documentation/gamekit/gksenddatamode)

##### Constants

- [case reliable](/documentation/gamekit/gksenddatamode/reliable)
- [case unreliable](/documentation/gamekit/gksenddatamode/unreliable)

##### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gksenddatamode/init(rawvalue:))
- [GKSessionMode](/documentation/gamekit/gksessionmode)

##### Constants

- [case server](/documentation/gamekit/gksessionmode/server)
- [case client](/documentation/gamekit/gksessionmode/client)
- [case peer](/documentation/gamekit/gksessionmode/peer)

##### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gksessionmode/init(rawvalue:))
- [GKPeerConnectionState](/documentation/gamekit/gkpeerconnectionstate)

##### Constants

- [case stateAvailable](/documentation/gamekit/gkpeerconnectionstate/stateavailable)
- [case stateUnavailable](/documentation/gamekit/gkpeerconnectionstate/stateunavailable)
- [case stateConnected](/documentation/gamekit/gkpeerconnectionstate/stateconnected)
- [case stateDisconnected](/documentation/gamekit/gkpeerconnectionstate/statedisconnected)
- [case stateConnecting](/documentation/gamekit/gkpeerconnectionstate/stateconnecting)

##### Enumeration Cases

- [case stateConnectedRelay](/documentation/gamekit/gkpeerconnectionstate/stateconnectedrelay)

##### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gkpeerconnectionstate/init(rawvalue:))
- [The Session Error Domain](/documentation/gamekit/the-session-error-domain)

##### Constants

- [let GKSessionErrorDomain: String](/documentation/gamekit/gksessionerrordomain)
- [GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/code)

##### Constants

- [case invalidParameterError](/documentation/gamekit/gksessionerror-swift.struct/code/invalidparametererror)
- [case peerNotFoundError](/documentation/gamekit/gksessionerror-swift.struct/code/peernotfounderror)
- [case declinedError](/documentation/gamekit/gksessionerror-swift.struct/code/declinederror)
- [case timedOutError](/documentation/gamekit/gksessionerror-swift.struct/code/timedouterror)
- [case cancelledError](/documentation/gamekit/gksessionerror-swift.struct/code/cancellederror)
- [case connectionFailedError](/documentation/gamekit/gksessionerror-swift.struct/code/connectionfailederror)
- [case connectionClosedError](/documentation/gamekit/gksessionerror-swift.struct/code/connectionclosederror)
- [case dataTooBigError](/documentation/gamekit/gksessionerror-swift.struct/code/datatoobigerror)
- [case notConnectedError](/documentation/gamekit/gksessionerror-swift.struct/code/notconnectederror)
- [case cannotEnableError](/documentation/gamekit/gksessionerror-swift.struct/code/cannotenableerror)
- [case inProgressError](/documentation/gamekit/gksessionerror-swift.struct/code/inprogresserror)
- [case connectivityError](/documentation/gamekit/gksessionerror-swift.struct/code/connectivityerror)
- [case transportError](/documentation/gamekit/gksessionerror-swift.struct/code/transporterror)
- [case internalError](/documentation/gamekit/gksessionerror-swift.struct/code/internalerror)
- [case unknownError](/documentation/gamekit/gksessionerror-swift.struct/code/unknownerror)
- [case systemError](/documentation/gamekit/gksessionerror-swift.struct/code/systemerror)

##### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gksessionerror-swift.struct/code/init(rawvalue:))
- [GKSessionError](/documentation/gamekit/gksessionerror-swift.struct)

##### Type Properties

- [static var cancelledError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/cancellederror)
- [static var cannotEnableError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/cannotenableerror)
- [static var connectionClosedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/connectionclosederror)
- [static var connectionFailedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/connectionfailederror)
- [static var connectivityError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/connectivityerror)
- [static var dataTooBigError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/datatoobigerror)
- [static var declinedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/declinederror)
- [static var errorDomain: String](/documentation/gamekit/gksessionerror-swift.struct/errordomain)
- [static var inProgressError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/inprogresserror)
- [static var internalError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/internalerror)
- [static var invalidParameterError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/invalidparametererror)
- [static var notConnectedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/notconnectederror)
- [static var peerNotFoundError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/peernotfounderror)
- [static var systemError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/systemerror)
- [static var timedOutError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/timedouterror)
- [static var transportError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/transporterror)
- [static var unknownError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/unknownerror)

##### Enumerations

- [GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/code)

###### Constants

- [case invalidParameterError](/documentation/gamekit/gksessionerror-swift.struct/code/invalidparametererror)
- [case peerNotFoundError](/documentation/gamekit/gksessionerror-swift.struct/code/peernotfounderror)
- [case declinedError](/documentation/gamekit/gksessionerror-swift.struct/code/declinederror)
- [case timedOutError](/documentation/gamekit/gksessionerror-swift.struct/code/timedouterror)
- [case cancelledError](/documentation/gamekit/gksessionerror-swift.struct/code/cancellederror)
- [case connectionFailedError](/documentation/gamekit/gksessionerror-swift.struct/code/connectionfailederror)
- [case connectionClosedError](/documentation/gamekit/gksessionerror-swift.struct/code/connectionclosederror)
- [case dataTooBigError](/documentation/gamekit/gksessionerror-swift.struct/code/datatoobigerror)
- [case notConnectedError](/documentation/gamekit/gksessionerror-swift.struct/code/notconnectederror)
- [case cannotEnableError](/documentation/gamekit/gksessionerror-swift.struct/code/cannotenableerror)
- [case inProgressError](/documentation/gamekit/gksessionerror-swift.struct/code/inprogresserror)
- [case connectivityError](/documentation/gamekit/gksessionerror-swift.struct/code/connectivityerror)
- [case transportError](/documentation/gamekit/gksessionerror-swift.struct/code/transporterror)
- [case internalError](/documentation/gamekit/gksessionerror-swift.struct/code/internalerror)
- [case unknownError](/documentation/gamekit/gksessionerror-swift.struct/code/unknownerror)
- [case systemError](/documentation/gamekit/gksessionerror-swift.struct/code/systemerror)

###### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gksessionerror-swift.struct/code/init(rawvalue:))
- [GKTurnBasedEventHandler](/documentation/gamekit/gkturnbasedeventhandler)

#### Retrieving the Shared Instance

- [class func shared() -> GKTurnBasedEventHandler](/documentation/gamekit/gkturnbasedeventhandler/shared())

#### Getting and Setting the Delegate

- [var delegate: (any GKTurnBasedEventHandlerDelegate & NSObjectProtocol)?](/documentation/gamekit/gkturnbasedeventhandler/delegate)
- [GKVoiceChat](/documentation/gamekit/gkvoicechat)

#### Determining Whether Voice Chat Is Available

- [class func isVoIPAllowed() -> Bool](/documentation/gamekit/gkvoicechat/isvoipallowed())

#### Starting and Stopping Voice Chat

- [func start()](/documentation/gamekit/gkvoicechat/start())
- [func stop()](/documentation/gamekit/gkvoicechat/stop())
- [var isActive: Bool](/documentation/gamekit/gkvoicechat/isactive)

#### Receiving Updates About Other Participants

- [var playerVoiceChatStateDidChangeHandler: (GKPlayer, GKVoiceChat.PlayerState) -> Void](/documentation/gamekit/gkvoicechat/playervoicechatstatedidchangehandler)
- [GKVoiceChat.PlayerState](/documentation/gamekit/gkvoicechat/playerstate)

##### States

- [case connected](/documentation/gamekit/gkvoicechat/playerstate/connected)
- [case disconnected](/documentation/gamekit/gkvoicechat/playerstate/disconnected)
- [case speaking](/documentation/gamekit/gkvoicechat/playerstate/speaking)
- [case silent](/documentation/gamekit/gkvoicechat/playerstate/silent)
- [case connecting](/documentation/gamekit/gkvoicechat/playerstate/connecting)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkvoicechat/playerstate/init(rawvalue:))

#### Controlling Chat Volume

- [func setPlayer(GKPlayer, muted: Bool)](/documentation/gamekit/gkvoicechat/setplayer(_:muted:))
- [var volume: Float](/documentation/gamekit/gkvoicechat/volume)

#### Accessing Properties

- [var name: String](/documentation/gamekit/gkvoicechat/name)
- [var players: [GKPlayer]](/documentation/gamekit/gkvoicechat/players)

#### Deprecated Methods and Properties

- [var playerIDs: [String]?](/documentation/gamekit/gkvoicechat/playerids)
- [var playerStateUpdateHandler: (String, GKVoiceChat.PlayerState) -> Void](/documentation/gamekit/gkvoicechat/playerstateupdatehandler)
- [func setMute(Bool, forPlayer: String)](/documentation/gamekit/gkvoicechat/setmute(_:forplayer:))
- [GKVoiceChatService](/documentation/gamekit/gkvoicechatservice)

#### Determining Whether Voice Chat Is Available

- [class func isVoIPAllowed() -> Bool](/documentation/gamekit/gkvoicechatservice/isvoipallowed())

#### Getting the Shared Voice Chat Service

- [class func `default`() -> GKVoiceChatService!](/documentation/gamekit/gkvoicechatservice/default())

#### Setting the Client

- [var client: (any GKVoiceChatClient)!](/documentation/gamekit/gkvoicechatservice/client)

#### Establishing a Voice Chat

- [func startVoiceChat(withParticipantID: String!) throws](/documentation/gamekit/gkvoicechatservice/startvoicechat(withparticipantid:))

#### Adjusting Audio Properties

- [var isMicrophoneMuted: Bool](/documentation/gamekit/gkvoicechatservice/ismicrophonemuted)
- [var remoteParticipantVolume: Float](/documentation/gamekit/gkvoicechatservice/remoteparticipantvolume)

#### Monitoring the Audio Level

- [var isInputMeteringEnabled: Bool](/documentation/gamekit/gkvoicechatservice/isinputmeteringenabled)
- [var inputMeterLevel: Float](/documentation/gamekit/gkvoicechatservice/inputmeterlevel)
- [var isOutputMeteringEnabled: Bool](/documentation/gamekit/gkvoicechatservice/isoutputmeteringenabled)
- [var outputMeterLevel: Float](/documentation/gamekit/gkvoicechatservice/outputmeterlevel)

#### Ending a Voice Chat

- [func stopVoiceChat(withParticipantID: String!)](/documentation/gamekit/gkvoicechatservice/stopvoicechat(withparticipantid:))

#### Methods Called by the Client

- [func acceptCallID(Int) throws](/documentation/gamekit/gkvoicechatservice/acceptcallid(_:))
- [func denyCallID(Int)](/documentation/gamekit/gkvoicechatservice/denycallid(_:))
- [func receivedData(Data!, fromParticipantID: String!)](/documentation/gamekit/gkvoicechatservice/receiveddata(_:fromparticipantid:))
- [func receivedRealTime(Data!, fromParticipantID: String!)](/documentation/gamekit/gkvoicechatservice/receivedrealtime(_:fromparticipantid:))

#### Constants

- [Voice Chat Service Error Domain](/documentation/gamekit/voice-chat-service-error-domain)

##### Constants

- [let GKVoiceChatServiceErrorDomain: String](/documentation/gamekit/gkvoicechatserviceerrordomain)
- [GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code)

##### Constants

- [case internalError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/internalerror)
- [case noRemotePacketsError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/noremotepacketserror)
- [case unableToConnectError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/unabletoconnecterror)
- [case remoteParticipantHangupError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipanthanguperror)
- [case invalidCallIDError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/invalidcalliderror)
- [case audioUnavailableError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/audiounavailableerror)
- [case uninitializedClientError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/uninitializedclienterror)
- [case clientMissingRequiredMethodsError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/clientmissingrequiredmethodserror)
- [case remoteParticipantBusyError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantbusyerror)
- [case remoteParticipantCancelledError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantcancellederror)
- [case remoteParticipantResponseInvalidError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantresponseinvaliderror)
- [case remoteParticipantDeclinedInviteError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantdeclinedinviteerror)
- [case methodCurrentlyInvalidError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/methodcurrentlyinvaliderror)
- [case networkConfigurationError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/networkconfigurationerror)
- [case unsupportedRemoteVersionError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/unsupportedremoteversionerror)
- [case outOfMemoryError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/outofmemoryerror)
- [case invalidParameterError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/invalidparametererror)

##### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/init(rawvalue:))
- [GKVoiceChatServiceError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct)

##### Type Properties

- [static var audioUnavailableError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/audiounavailableerror)
- [static var clientMissingRequiredMethodsError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/clientmissingrequiredmethodserror)
- [static var errorDomain: String](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/errordomain)
- [static var internalError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/internalerror)
- [static var invalidCallIDError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/invalidcalliderror)
- [static var invalidParameterError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/invalidparametererror)
- [static var methodCurrentlyInvalidError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/methodcurrentlyinvaliderror)
- [static var networkConfigurationError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/networkconfigurationerror)
- [static var noRemotePacketsError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/noremotepacketserror)
- [static var outOfMemoryError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/outofmemoryerror)
- [static var remoteParticipantBusyError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantbusyerror)
- [static var remoteParticipantCancelledError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantcancellederror)
- [static var remoteParticipantDeclinedInviteError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantdeclinedinviteerror)
- [static var remoteParticipantHangupError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipanthanguperror)
- [static var remoteParticipantResponseInvalidError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantresponseinvaliderror)
- [static var unableToConnectError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/unabletoconnecterror)
- [static var uninitializedClientError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/uninitializedclienterror)
- [static var unsupportedRemoteVersionError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/unsupportedremoteversionerror)

##### Enumerations

- [GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code)

###### Constants

- [case internalError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/internalerror)
- [case noRemotePacketsError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/noremotepacketserror)
- [case unableToConnectError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/unabletoconnecterror)
- [case remoteParticipantHangupError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipanthanguperror)
- [case invalidCallIDError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/invalidcalliderror)
- [case audioUnavailableError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/audiounavailableerror)
- [case uninitializedClientError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/uninitializedclienterror)
- [case clientMissingRequiredMethodsError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/clientmissingrequiredmethodserror)
- [case remoteParticipantBusyError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantbusyerror)
- [case remoteParticipantCancelledError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantcancellederror)
- [case remoteParticipantResponseInvalidError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantresponseinvaliderror)
- [case remoteParticipantDeclinedInviteError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantdeclinedinviteerror)
- [case methodCurrentlyInvalidError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/methodcurrentlyinvaliderror)
- [case networkConfigurationError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/networkconfigurationerror)
- [case unsupportedRemoteVersionError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/unsupportedremoteversionerror)
- [case outOfMemoryError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/outofmemoryerror)
- [case invalidParameterError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/invalidparametererror)

###### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/init(rawvalue:))
- [GKNotificationBanner](/documentation/gamekit/gknotificationbanner)

#### Displaying the Banner

- [class func show(withTitle: String?, message: String?, completionHandler: (() -> Void)?)](/documentation/gamekit/gknotificationbanner/show(withtitle:message:completionhandler:))
- [class func show(withTitle: String?, message: String?, duration: TimeInterval, completionHandler: (() -> Void)?)](/documentation/gamekit/gknotificationbanner/show(withtitle:message:duration:completionhandler:))

### Deprecated protocols

- [GKAchievementViewControllerDelegate](/documentation/gamekit/gkachievementviewcontrollerdelegate)

#### Responding to a Dismiss Action

- [func achievementViewControllerDidFinish(GKAchievementViewController!)](/documentation/gamekit/gkachievementviewcontrollerdelegate/achievementviewcontrollerdidfinish(_:))
- [GKChallengeEventHandlerDelegate](/documentation/gamekit/gkchallengeeventhandlerdelegate)

#### Detecting When a User Taps a Banner

- [func localPlayerDidSelect(GKChallenge!)](/documentation/gamekit/gkchallengeeventhandlerdelegate/localplayerdidselect(_:))

#### Responding When a New Challenge is Received

- [func localPlayerDidReceive(GKChallenge!)](/documentation/gamekit/gkchallengeeventhandlerdelegate/localplayerdidreceive(_:))
- [func shouldShowBanner(forLocallyReceivedChallenge: GKChallenge!) -> Bool](/documentation/gamekit/gkchallengeeventhandlerdelegate/shouldshowbanner(forlocallyreceivedchallenge:))

#### Responding to Challenges Completed By the Local Player

- [func localPlayerDidComplete(GKChallenge!)](/documentation/gamekit/gkchallengeeventhandlerdelegate/localplayerdidcomplete(_:))
- [func shouldShowBanner(forLocallyCompletedChallenge: GKChallenge!) -> Bool](/documentation/gamekit/gkchallengeeventhandlerdelegate/shouldshowbanner(forlocallycompletedchallenge:))

#### Responding to Challenges Issued by the Local Player

- [func remotePlayerDidComplete(GKChallenge!)](/documentation/gamekit/gkchallengeeventhandlerdelegate/remoteplayerdidcomplete(_:))
- [func shouldShowBanner(forRemotelyCompletedChallenge: GKChallenge!) -> Bool](/documentation/gamekit/gkchallengeeventhandlerdelegate/shouldshowbanner(forremotelycompletedchallenge:))
- [GKChallengesViewControllerDelegate](/documentation/gamekit/gkchallengesviewcontrollerdelegate)

#### Dismissing the View Controller

- [func challengesViewControllerDidFinish(GKChallengesViewController!)](/documentation/gamekit/gkchallengesviewcontrollerdelegate/challengesviewcontrollerdidfinish(_:))
- [GKChallengeListener](/documentation/gamekit/gkchallengelistener)

#### Responding to a Challenge

- [func player(GKPlayer, didReceive: GKChallenge)](/documentation/gamekit/gkchallengelistener/player(_:didreceive:))
- [func player(GKPlayer, wantsToPlay: GKChallenge)](/documentation/gamekit/gkchallengelistener/player(_:wantstoplay:))

#### Completing a Challenge

- [func player(GKPlayer, didComplete: GKChallenge, issuedByFriend: GKPlayer)](/documentation/gamekit/gkchallengelistener/player(_:didcomplete:issuedbyfriend:))
- [func player(GKPlayer, issuedChallengeWasCompleted: GKChallenge, byFriend: GKPlayer)](/documentation/gamekit/gkchallengelistener/player(_:issuedchallengewascompleted:byfriend:))
- [GKFriendRequestComposeViewControllerDelegate](/documentation/gamekit/gkfriendrequestcomposeviewcontrollerdelegate)

#### Instance Methods

- [func friendRequestComposeViewControllerDidFinish(GKFriendRequestComposeViewController)](/documentation/gamekit/gkfriendrequestcomposeviewcontrollerdelegate/friendrequestcomposeviewcontrollerdidfinish(_:))
- [GKGameSessionEventListener](/documentation/gamekit/gkgamesessioneventlistener)

#### Changing Player Status

- [func session(GKGameSession, didAdd: GKCloudPlayer)](/documentation/gamekit/gkgamesessioneventlistener/session(_:didadd:))
- [func session(GKGameSession, didRemove: GKCloudPlayer)](/documentation/gamekit/gkgamesessioneventlistener/session(_:didremove:))
- [func session(GKGameSession, player: GKCloudPlayer, didChange: GKConnectionState)](/documentation/gamekit/gkgamesessioneventlistener/session(_:player:didchange:))
- [GKConnectionState](/documentation/gamekit/gkconnectionstate)

##### Constants

- [case connected](/documentation/gamekit/gkconnectionstate/connected)
- [case notConnected](/documentation/gamekit/gkconnectionstate/notconnected)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkconnectionstate/init(rawvalue:))

#### Transferring Data

- [func session(GKGameSession, didReceive: Data, from: GKCloudPlayer)](/documentation/gamekit/gkgamesessioneventlistener/session(_:didreceive:from:))
- [func session(GKGameSession, didReceiveMessage: String, with: Data, from: GKCloudPlayer)](/documentation/gamekit/gkgamesessioneventlistener/session(_:didreceivemessage:with:from:))
- [func session(GKGameSession, player: GKCloudPlayer, didSave: Data)](/documentation/gamekit/gkgamesessioneventlistener/session(_:player:didsave:))
- [GKLeaderboardViewControllerDelegate](/documentation/gamekit/gkleaderboardviewcontrollerdelegate)

#### Handling User Actions

- [func leaderboardViewControllerDidFinish(GKLeaderboardViewController!)](/documentation/gamekit/gkleaderboardviewcontrollerdelegate/leaderboardviewcontrollerdidfinish(_:))
- [GKPeerPickerControllerDelegate](/documentation/gamekit/gkpeerpickercontrollerdelegate)

#### Creating a Session for the Peer Picker

- [func peerPickerController(GKPeerPickerController, didSelect: GKPeerPickerConnectionType)](/documentation/gamekit/gkpeerpickercontrollerdelegate/peerpickercontroller(_:didselect:))
- [func peerPickerController(GKPeerPickerController, sessionFor: GKPeerPickerConnectionType) -> GKSession](/documentation/gamekit/gkpeerpickercontrollerdelegate/peerpickercontroller(_:sessionfor:))

#### Responding to Connection Messages

- [func peerPickerController(GKPeerPickerController, didConnectPeer: String, to: GKSession)](/documentation/gamekit/gkpeerpickercontrollerdelegate/peerpickercontroller(_:didconnectpeer:to:))

#### Responding When the User Cancels the Connection Attempt

- [func peerPickerControllerDidCancel(GKPeerPickerController)](/documentation/gamekit/gkpeerpickercontrollerdelegate/peerpickercontrollerdidcancel(_:))
- [GKSessionDelegate](/documentation/gamekit/gksessiondelegate)

#### Observing Changes to Peers

- [func session(GKSession, peer: String, didChange: GKPeerConnectionState)](/documentation/gamekit/gksessiondelegate/session(_:peer:didchange:))

#### Connection Requests from Other Peers

- [func session(GKSession, didReceiveConnectionRequestFromPeer: String)](/documentation/gamekit/gksessiondelegate/session(_:didreceiveconnectionrequestfrompeer:))

#### Connection Errors

- [func session(GKSession, connectionWithPeerFailed: String, withError: any Error)](/documentation/gamekit/gksessiondelegate/session(_:connectionwithpeerfailed:witherror:))
- [func session(GKSession, didFailWithError: any Error)](/documentation/gamekit/gksessiondelegate/session(_:didfailwitherror:))
- [GKTurnBasedEventHandlerDelegate](/documentation/gamekit/gkturnbasedeventhandlerdelegate)

#### Receiving Turn-based Events

- [func handleInvite(fromGameCenter: [String])](/documentation/gamekit/gkturnbasedeventhandlerdelegate/handleinvite(fromgamecenter:))
- [func handleTurnEvent(for: GKTurnBasedMatch)](/documentation/gamekit/gkturnbasedeventhandlerdelegate/handleturnevent(for:))
- [func handleTurnEvent(for: GKTurnBasedMatch, didBecomeActive: Bool)](/documentation/gamekit/gkturnbasedeventhandlerdelegate/handleturnevent(for:didbecomeactive:))
- [func handleMatchEnded(GKTurnBasedMatch)](/documentation/gamekit/gkturnbasedeventhandlerdelegate/handlematchended(_:))
- [GKVoiceChatClient](/documentation/gamekit/gkvoicechatclient)

#### Getting Information about the Participant

- [func participantID() -> String](/documentation/gamekit/gkvoicechatclient/participantid())

#### Sending data to other participants

- [func voiceChatService(GKVoiceChatService, send: Data, toParticipantID: String)](/documentation/gamekit/gkvoicechatclient/voicechatservice(_:send:toparticipantid:))
- [func voiceChatService(GKVoiceChatService, sendRealTime: Data, toParticipantID: String)](/documentation/gamekit/gkvoicechatclient/voicechatservice(_:sendrealtime:toparticipantid:))

#### Accepting Invitations from Remote Participants

- [func voiceChatService(GKVoiceChatService, didReceiveInvitationFromParticipantID: String, callID: Int)](/documentation/gamekit/gkvoicechatclient/voicechatservice(_:didreceiveinvitationfromparticipantid:callid:))

#### Responding to Changes in Other Participants

- [func voiceChatService(GKVoiceChatService, didStartWithParticipantID: String)](/documentation/gamekit/gkvoicechatclient/voicechatservice(_:didstartwithparticipantid:))
- [func voiceChatService(GKVoiceChatService, didNotStartWithParticipantID: String, error: (any Error)?)](/documentation/gamekit/gkvoicechatclient/voicechatservice(_:didnotstartwithparticipantid:error:))
- [func voiceChatService(GKVoiceChatService, didStopWithParticipantID: String, error: (any Error)?)](/documentation/gamekit/gkvoicechatclient/voicechatservice(_:didstopwithparticipantid:error:))

### Deprecated structures

- [GKVoiceChatServiceError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct)

#### Type Properties

- [static var audioUnavailableError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/audiounavailableerror)
- [static var clientMissingRequiredMethodsError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/clientmissingrequiredmethodserror)
- [static var errorDomain: String](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/errordomain)
- [static var internalError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/internalerror)
- [static var invalidCallIDError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/invalidcalliderror)
- [static var invalidParameterError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/invalidparametererror)
- [static var methodCurrentlyInvalidError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/methodcurrentlyinvaliderror)
- [static var networkConfigurationError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/networkconfigurationerror)
- [static var noRemotePacketsError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/noremotepacketserror)
- [static var outOfMemoryError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/outofmemoryerror)
- [static var remoteParticipantBusyError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantbusyerror)
- [static var remoteParticipantCancelledError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantcancellederror)
- [static var remoteParticipantDeclinedInviteError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantdeclinedinviteerror)
- [static var remoteParticipantHangupError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipanthanguperror)
- [static var remoteParticipantResponseInvalidError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantresponseinvaliderror)
- [static var unableToConnectError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/unabletoconnecterror)
- [static var uninitializedClientError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/uninitializedclienterror)
- [static var unsupportedRemoteVersionError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/unsupportedremoteversionerror)

#### Enumerations

- [GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code)

##### Constants

- [case internalError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/internalerror)
- [case noRemotePacketsError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/noremotepacketserror)
- [case unableToConnectError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/unabletoconnecterror)
- [case remoteParticipantHangupError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipanthanguperror)
- [case invalidCallIDError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/invalidcalliderror)
- [case audioUnavailableError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/audiounavailableerror)
- [case uninitializedClientError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/uninitializedclienterror)
- [case clientMissingRequiredMethodsError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/clientmissingrequiredmethodserror)
- [case remoteParticipantBusyError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantbusyerror)
- [case remoteParticipantCancelledError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantcancellederror)
- [case remoteParticipantResponseInvalidError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantresponseinvaliderror)
- [case remoteParticipantDeclinedInviteError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantdeclinedinviteerror)
- [case methodCurrentlyInvalidError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/methodcurrentlyinvaliderror)
- [case networkConfigurationError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/networkconfigurationerror)
- [case unsupportedRemoteVersionError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/unsupportedremoteversionerror)
- [case outOfMemoryError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/outofmemoryerror)
- [case invalidParameterError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/invalidparametererror)

##### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/init(rawvalue:))
- [GKSessionError](/documentation/gamekit/gksessionerror-swift.struct)

#### Type Properties

- [static var cancelledError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/cancellederror)
- [static var cannotEnableError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/cannotenableerror)
- [static var connectionClosedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/connectionclosederror)
- [static var connectionFailedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/connectionfailederror)
- [static var connectivityError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/connectivityerror)
- [static var dataTooBigError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/datatoobigerror)
- [static var declinedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/declinederror)
- [static var errorDomain: String](/documentation/gamekit/gksessionerror-swift.struct/errordomain)
- [static var inProgressError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/inprogresserror)
- [static var internalError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/internalerror)
- [static var invalidParameterError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/invalidparametererror)
- [static var notConnectedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/notconnectederror)
- [static var peerNotFoundError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/peernotfounderror)
- [static var systemError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/systemerror)
- [static var timedOutError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/timedouterror)
- [static var transportError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/transporterror)
- [static var unknownError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/unknownerror)

#### Enumerations

- [GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/code)

##### Constants

- [case invalidParameterError](/documentation/gamekit/gksessionerror-swift.struct/code/invalidparametererror)
- [case peerNotFoundError](/documentation/gamekit/gksessionerror-swift.struct/code/peernotfounderror)
- [case declinedError](/documentation/gamekit/gksessionerror-swift.struct/code/declinederror)
- [case timedOutError](/documentation/gamekit/gksessionerror-swift.struct/code/timedouterror)
- [case cancelledError](/documentation/gamekit/gksessionerror-swift.struct/code/cancellederror)
- [case connectionFailedError](/documentation/gamekit/gksessionerror-swift.struct/code/connectionfailederror)
- [case connectionClosedError](/documentation/gamekit/gksessionerror-swift.struct/code/connectionclosederror)
- [case dataTooBigError](/documentation/gamekit/gksessionerror-swift.struct/code/datatoobigerror)
- [case notConnectedError](/documentation/gamekit/gksessionerror-swift.struct/code/notconnectederror)
- [case cannotEnableError](/documentation/gamekit/gksessionerror-swift.struct/code/cannotenableerror)
- [case inProgressError](/documentation/gamekit/gksessionerror-swift.struct/code/inprogresserror)
- [case connectivityError](/documentation/gamekit/gksessionerror-swift.struct/code/connectivityerror)
- [case transportError](/documentation/gamekit/gksessionerror-swift.struct/code/transporterror)
- [case internalError](/documentation/gamekit/gksessionerror-swift.struct/code/internalerror)
- [case unknownError](/documentation/gamekit/gksessionerror-swift.struct/code/unknownerror)
- [case systemError](/documentation/gamekit/gksessionerror-swift.struct/code/systemerror)

##### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gksessionerror-swift.struct/code/init(rawvalue:))
- [GKGameSessionError](/documentation/gamekit/gkgamesessionerror)

#### Error Codes

- [static var badContainer: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/badcontainer)
- [static var cloudDriveDisabled: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/clouddrivedisabled)
- [static var cloudQuotaExceeded: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/cloudquotaexceeded)
- [static var connectionCancelledByUser: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/connectioncancelledbyuser)
- [static var connectionFailed: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/connectionfailed)
- [static var invalidSession: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/invalidsession)
- [static var networkFailure: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/networkfailure)
- [static var notAuthenticated: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/notauthenticated)
- [static var sendDataNoRecipients: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/senddatanorecipients)
- [static var sendDataNotConnected: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/senddatanotconnected)
- [static var sendDataNotReachable: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/senddatanotreachable)
- [static var sendRateLimitReached: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/sendratelimitreached)
- [static var sessionConflict: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/sessionconflict)
- [static var sessionHasMaxConnectedPlayers: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/sessionhasmaxconnectedplayers)
- [static var sessionNotShared: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/sessionnotshared)
- [static var unknown: GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/unknown)
- [GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/code)

##### Enumeration Cases

- [case unknown](/documentation/gamekit/gkgamesessionerror/code/unknown)
- [case notAuthenticated](/documentation/gamekit/gkgamesessionerror/code/notauthenticated)
- [case sessionConflict](/documentation/gamekit/gkgamesessionerror/code/sessionconflict)
- [case sessionNotShared](/documentation/gamekit/gkgamesessionerror/code/sessionnotshared)
- [case connectionCancelledByUser](/documentation/gamekit/gkgamesessionerror/code/connectioncancelledbyuser)
- [case connectionFailed](/documentation/gamekit/gkgamesessionerror/code/connectionfailed)
- [case sessionHasMaxConnectedPlayers](/documentation/gamekit/gkgamesessionerror/code/sessionhasmaxconnectedplayers)
- [case sendDataNotConnected](/documentation/gamekit/gkgamesessionerror/code/senddatanotconnected)
- [case sendDataNoRecipients](/documentation/gamekit/gkgamesessionerror/code/senddatanorecipients)
- [case sendDataNotReachable](/documentation/gamekit/gkgamesessionerror/code/senddatanotreachable)
- [case sendRateLimitReached](/documentation/gamekit/gkgamesessionerror/code/sendratelimitreached)
- [case badContainer](/documentation/gamekit/gkgamesessionerror/code/badcontainer)
- [case cloudQuotaExceeded](/documentation/gamekit/gkgamesessionerror/code/cloudquotaexceeded)
- [case networkFailure](/documentation/gamekit/gkgamesessionerror/code/networkfailure)
- [case cloudDriveDisabled](/documentation/gamekit/gkgamesessionerror/code/clouddrivedisabled)
- [case invalidSession](/documentation/gamekit/gkgamesessionerror/code/invalidsession)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkgamesessionerror/code/init(rawvalue:))

#### Error Domain

- [static var errorDomain: String](/documentation/gamekit/gkgamesessionerror/errordomain)
- [let GKGameSessionErrorDomain: String](/documentation/gamekit/gkgamesessionerrordomain)

### Deprecated constants

- [let GKGameSessionErrorDomain: String](/documentation/gamekit/gkgamesessionerrordomain)
- [let GKSessionErrorDomain: String](/documentation/gamekit/gksessionerrordomain)
- [let GKVoiceChatServiceErrorDomain: String](/documentation/gamekit/gkvoicechatserviceerrordomain)

### Deprecated enumerations

- [GKGameSessionError.Code](/documentation/gamekit/gkgamesessionerror/code)

#### Enumeration Cases

- [case unknown](/documentation/gamekit/gkgamesessionerror/code/unknown)
- [case notAuthenticated](/documentation/gamekit/gkgamesessionerror/code/notauthenticated)
- [case sessionConflict](/documentation/gamekit/gkgamesessionerror/code/sessionconflict)
- [case sessionNotShared](/documentation/gamekit/gkgamesessionerror/code/sessionnotshared)
- [case connectionCancelledByUser](/documentation/gamekit/gkgamesessionerror/code/connectioncancelledbyuser)
- [case connectionFailed](/documentation/gamekit/gkgamesessionerror/code/connectionfailed)
- [case sessionHasMaxConnectedPlayers](/documentation/gamekit/gkgamesessionerror/code/sessionhasmaxconnectedplayers)
- [case sendDataNotConnected](/documentation/gamekit/gkgamesessionerror/code/senddatanotconnected)
- [case sendDataNoRecipients](/documentation/gamekit/gkgamesessionerror/code/senddatanorecipients)
- [case sendDataNotReachable](/documentation/gamekit/gkgamesessionerror/code/senddatanotreachable)
- [case sendRateLimitReached](/documentation/gamekit/gkgamesessionerror/code/sendratelimitreached)
- [case badContainer](/documentation/gamekit/gkgamesessionerror/code/badcontainer)
- [case cloudQuotaExceeded](/documentation/gamekit/gkgamesessionerror/code/cloudquotaexceeded)
- [case networkFailure](/documentation/gamekit/gkgamesessionerror/code/networkfailure)
- [case cloudDriveDisabled](/documentation/gamekit/gkgamesessionerror/code/clouddrivedisabled)
- [case invalidSession](/documentation/gamekit/gkgamesessionerror/code/invalidsession)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamekit/gkgamesessionerror/code/init(rawvalue:))
- [GKPeerConnectionState](/documentation/gamekit/gkpeerconnectionstate)

#### Constants

- [case stateAvailable](/documentation/gamekit/gkpeerconnectionstate/stateavailable)
- [case stateUnavailable](/documentation/gamekit/gkpeerconnectionstate/stateunavailable)
- [case stateConnected](/documentation/gamekit/gkpeerconnectionstate/stateconnected)
- [case stateDisconnected](/documentation/gamekit/gkpeerconnectionstate/statedisconnected)
- [case stateConnecting](/documentation/gamekit/gkpeerconnectionstate/stateconnecting)

#### Enumeration Cases

- [case stateConnectedRelay](/documentation/gamekit/gkpeerconnectionstate/stateconnectedrelay)

#### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gkpeerconnectionstate/init(rawvalue:))
- [GKPeerPickerConnectionType](/documentation/gamekit/gkpeerpickerconnectiontype)

#### Constants

- [case nearby](/documentation/gamekit/gkpeerpickerconnectiontype/nearby)
- [case online](/documentation/gamekit/gkpeerpickerconnectiontype/online)
- [case nearby](/documentation/gamekit/gkpeerpickerconnectiontype/nearby)

#### Initializers

- [init?(rawValue: UInt)](/documentation/gamekit/gkpeerpickerconnectiontype/init(rawvalue:))
- [GKSendDataMode](/documentation/gamekit/gksenddatamode)

#### Constants

- [case reliable](/documentation/gamekit/gksenddatamode/reliable)
- [case unreliable](/documentation/gamekit/gksenddatamode/unreliable)

#### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gksenddatamode/init(rawvalue:))
- [GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/code)

#### Constants

- [case invalidParameterError](/documentation/gamekit/gksessionerror-swift.struct/code/invalidparametererror)
- [case peerNotFoundError](/documentation/gamekit/gksessionerror-swift.struct/code/peernotfounderror)
- [case declinedError](/documentation/gamekit/gksessionerror-swift.struct/code/declinederror)
- [case timedOutError](/documentation/gamekit/gksessionerror-swift.struct/code/timedouterror)
- [case cancelledError](/documentation/gamekit/gksessionerror-swift.struct/code/cancellederror)
- [case connectionFailedError](/documentation/gamekit/gksessionerror-swift.struct/code/connectionfailederror)
- [case connectionClosedError](/documentation/gamekit/gksessionerror-swift.struct/code/connectionclosederror)
- [case dataTooBigError](/documentation/gamekit/gksessionerror-swift.struct/code/datatoobigerror)
- [case notConnectedError](/documentation/gamekit/gksessionerror-swift.struct/code/notconnectederror)
- [case cannotEnableError](/documentation/gamekit/gksessionerror-swift.struct/code/cannotenableerror)
- [case inProgressError](/documentation/gamekit/gksessionerror-swift.struct/code/inprogresserror)
- [case connectivityError](/documentation/gamekit/gksessionerror-swift.struct/code/connectivityerror)
- [case transportError](/documentation/gamekit/gksessionerror-swift.struct/code/transporterror)
- [case internalError](/documentation/gamekit/gksessionerror-swift.struct/code/internalerror)
- [case unknownError](/documentation/gamekit/gksessionerror-swift.struct/code/unknownerror)
- [case systemError](/documentation/gamekit/gksessionerror-swift.struct/code/systemerror)

#### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gksessionerror-swift.struct/code/init(rawvalue:))
- [GKSessionError](/documentation/gamekit/gksessionerror-swift.struct)

#### Type Properties

- [static var cancelledError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/cancellederror)
- [static var cannotEnableError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/cannotenableerror)
- [static var connectionClosedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/connectionclosederror)
- [static var connectionFailedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/connectionfailederror)
- [static var connectivityError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/connectivityerror)
- [static var dataTooBigError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/datatoobigerror)
- [static var declinedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/declinederror)
- [static var errorDomain: String](/documentation/gamekit/gksessionerror-swift.struct/errordomain)
- [static var inProgressError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/inprogresserror)
- [static var internalError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/internalerror)
- [static var invalidParameterError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/invalidparametererror)
- [static var notConnectedError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/notconnectederror)
- [static var peerNotFoundError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/peernotfounderror)
- [static var systemError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/systemerror)
- [static var timedOutError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/timedouterror)
- [static var transportError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/transporterror)
- [static var unknownError: GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/unknownerror)

#### Enumerations

- [GKSessionError.Code](/documentation/gamekit/gksessionerror-swift.struct/code)

##### Constants

- [case invalidParameterError](/documentation/gamekit/gksessionerror-swift.struct/code/invalidparametererror)
- [case peerNotFoundError](/documentation/gamekit/gksessionerror-swift.struct/code/peernotfounderror)
- [case declinedError](/documentation/gamekit/gksessionerror-swift.struct/code/declinederror)
- [case timedOutError](/documentation/gamekit/gksessionerror-swift.struct/code/timedouterror)
- [case cancelledError](/documentation/gamekit/gksessionerror-swift.struct/code/cancellederror)
- [case connectionFailedError](/documentation/gamekit/gksessionerror-swift.struct/code/connectionfailederror)
- [case connectionClosedError](/documentation/gamekit/gksessionerror-swift.struct/code/connectionclosederror)
- [case dataTooBigError](/documentation/gamekit/gksessionerror-swift.struct/code/datatoobigerror)
- [case notConnectedError](/documentation/gamekit/gksessionerror-swift.struct/code/notconnectederror)
- [case cannotEnableError](/documentation/gamekit/gksessionerror-swift.struct/code/cannotenableerror)
- [case inProgressError](/documentation/gamekit/gksessionerror-swift.struct/code/inprogresserror)
- [case connectivityError](/documentation/gamekit/gksessionerror-swift.struct/code/connectivityerror)
- [case transportError](/documentation/gamekit/gksessionerror-swift.struct/code/transporterror)
- [case internalError](/documentation/gamekit/gksessionerror-swift.struct/code/internalerror)
- [case unknownError](/documentation/gamekit/gksessionerror-swift.struct/code/unknownerror)
- [case systemError](/documentation/gamekit/gksessionerror-swift.struct/code/systemerror)

##### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gksessionerror-swift.struct/code/init(rawvalue:))
- [GKSessionMode](/documentation/gamekit/gksessionmode)

#### Constants

- [case server](/documentation/gamekit/gksessionmode/server)
- [case client](/documentation/gamekit/gksessionmode/client)
- [case peer](/documentation/gamekit/gksessionmode/peer)

#### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gksessionmode/init(rawvalue:))
- [GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code)

#### Constants

- [case internalError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/internalerror)
- [case noRemotePacketsError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/noremotepacketserror)
- [case unableToConnectError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/unabletoconnecterror)
- [case remoteParticipantHangupError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipanthanguperror)
- [case invalidCallIDError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/invalidcalliderror)
- [case audioUnavailableError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/audiounavailableerror)
- [case uninitializedClientError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/uninitializedclienterror)
- [case clientMissingRequiredMethodsError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/clientmissingrequiredmethodserror)
- [case remoteParticipantBusyError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantbusyerror)
- [case remoteParticipantCancelledError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantcancellederror)
- [case remoteParticipantResponseInvalidError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantresponseinvaliderror)
- [case remoteParticipantDeclinedInviteError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantdeclinedinviteerror)
- [case methodCurrentlyInvalidError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/methodcurrentlyinvaliderror)
- [case networkConfigurationError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/networkconfigurationerror)
- [case unsupportedRemoteVersionError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/unsupportedremoteversionerror)
- [case outOfMemoryError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/outofmemoryerror)
- [case invalidParameterError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/invalidparametererror)

#### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/init(rawvalue:))
- [GKVoiceChatServiceError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct)

#### Type Properties

- [static var audioUnavailableError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/audiounavailableerror)
- [static var clientMissingRequiredMethodsError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/clientmissingrequiredmethodserror)
- [static var errorDomain: String](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/errordomain)
- [static var internalError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/internalerror)
- [static var invalidCallIDError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/invalidcalliderror)
- [static var invalidParameterError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/invalidparametererror)
- [static var methodCurrentlyInvalidError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/methodcurrentlyinvaliderror)
- [static var networkConfigurationError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/networkconfigurationerror)
- [static var noRemotePacketsError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/noremotepacketserror)
- [static var outOfMemoryError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/outofmemoryerror)
- [static var remoteParticipantBusyError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantbusyerror)
- [static var remoteParticipantCancelledError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantcancellederror)
- [static var remoteParticipantDeclinedInviteError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantdeclinedinviteerror)
- [static var remoteParticipantHangupError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipanthanguperror)
- [static var remoteParticipantResponseInvalidError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/remoteparticipantresponseinvaliderror)
- [static var unableToConnectError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/unabletoconnecterror)
- [static var uninitializedClientError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/uninitializedclienterror)
- [static var unsupportedRemoteVersionError: GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/unsupportedremoteversionerror)

#### Enumerations

- [GKVoiceChatServiceError.Code](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code)

##### Constants

- [case internalError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/internalerror)
- [case noRemotePacketsError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/noremotepacketserror)
- [case unableToConnectError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/unabletoconnecterror)
- [case remoteParticipantHangupError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipanthanguperror)
- [case invalidCallIDError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/invalidcalliderror)
- [case audioUnavailableError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/audiounavailableerror)
- [case uninitializedClientError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/uninitializedclienterror)
- [case clientMissingRequiredMethodsError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/clientmissingrequiredmethodserror)
- [case remoteParticipantBusyError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantbusyerror)
- [case remoteParticipantCancelledError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantcancellederror)
- [case remoteParticipantResponseInvalidError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantresponseinvaliderror)
- [case remoteParticipantDeclinedInviteError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/remoteparticipantdeclinedinviteerror)
- [case methodCurrentlyInvalidError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/methodcurrentlyinvaliderror)
- [case networkConfigurationError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/networkconfigurationerror)
- [case unsupportedRemoteVersionError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/unsupportedremoteversionerror)
- [case outOfMemoryError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/outofmemoryerror)
- [case invalidParameterError](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/invalidparametererror)

##### Initializers

- [init?(rawValue: Int32)](/documentation/gamekit/gkvoicechatserviceerror-swift.struct/code/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
