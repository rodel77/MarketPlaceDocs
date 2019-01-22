=============
Configuration
=============

~~~~~~~~~~~~~~~~~~~~~
Default Configuration
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: yaml

	allowPublish: true
	commands:
	  skiphelp: false
	  help: '&a/market &c{name} &3{arguments} &6(&7{help}&6)'
	  show-default-aliases: true
	  nopermission: '&cYou don''t permission to use this command'
	commands.skiphelp: false
	commands.help: '&a/market &c{name} &3{arguments} &6(&7{help}&6)'
	commands.show-default-aliases: true
	commands.nopermission: '&cYou don''t permission to use this command'
	command:
	  aliases: &id001
	  - mp
	  marketall: &id002
	    aliases: &id003
	    - marketall
	    permission: none
	  my: &id004
	    aliases: &id005
	    - self
	    description: Check your sold, unsold, history etc
	    argumentsHelp: ''
	  listings: &id006
	    aliases: &id007
	    - inspect
	    description: Open the menu of unbrought items of any player (You can remove listings)
	    argumentsHelp: <player_name|player_uuid>
	  publish: &id008
	    aliases: &id009
	    - sell
	    description: Publish a item in the marketplace
	    argumentsHelp: <price>
	  purge: &id010
	    aliases: &id011
	    - purge
	    description: 'Before use this command make sure you read this: http://marketplacedocs.readthedocs.io/en/latest/commands/purge.html'
	    argumentsHelp: <argument-name> [argument-value]
	  search: &id012
	    aliases: &id013
	    - search
	    description: Open the search menu
	    argumentsHelp: '[all|id|categories|name|lore|player] [name|lore|player-name]'
	    arguments: &id014
	      all: all
	      id: id
	      categories: categories
	      name: name
	      lore: lore
	      player: player
	  select: &id015
	    aliases: &id016
	    - select
	    description: 'Same args as purge, but it show the info instead on remove: http://marketplacedocs.readthedocs.io/en/latest/commands/purge.html'
	    argumentsHelp: <argument-name> [argument-value]...
	  limits: &id017
	    aliases: &id018
	    - limits
	    description: Manage player limits
	    argumentsHelp: <set|get|increment|decrement> <player> [slots]
	  reload: &id019
	    aliases: &id020
	    - reload
	    description: Reload configuration
	    argumentsHelp: ''
	  help: &id021
	    aliases: &id022
	    - help
	    description: Display this menu
	    argumentsHelp: ''
	  setpin: &id023
	    aliases: &id024
	    - webpin
	    description: Set the pin for login through the web client
	    argumentsHelp: <new-pin>
	  cancel: &id025
	    aliases: &id026
	    - borrow
	    description: Cancel all the listings (this is an experimental/migration command)
	    argumentsHelp: --all
	  wallet: &id027
	    aliases: &id028
	    - webmoney
	    description: Adds money to your web account, this allows you yo purchase items through the web system
	    argumentsHelp: <deposit|withdraw|check> [player|amount] [amount]
	    arguments: &id029
	      deposit: deposit
	      withdraw: withdraw
	      check: check
	command.aliases: *id001
	command.marketall: *id002
	command.marketall.aliases: *id003
	command.marketall.permission: none
	command.my: *id004
	command.my.aliases: *id005
	command.my.description: Check your sold, unsold, history etc
	command.my.argumentsHelp: ''
	command.listings: *id006
	command.listings.aliases: *id007
	command.listings.description: Open the menu of unbrought items of any player (You can remove listings)
	command.listings.argumentsHelp: <player_name|player_uuid>
	command.publish: *id008
	command.publish.aliases: *id009
	command.publish.description: Publish a item in the marketplace
	command.publish.argumentsHelp: <price>
	command.purge: *id010
	command.purge.aliases: *id011
	command.purge.description: 'Before use this command make sure you read this: http://marketplacedocs.readthedocs.io/en/latest/commands/purge.html'
	command.purge.argumentsHelp: <argument-name> [argument-value]
	command.search: *id012
	command.search.aliases: *id013
	command.search.description: Open the search menu
	command.search.argumentsHelp: '[all|id|categories|name|lore|player] [name|lore|player-name]'
	command.search.arguments: *id014
	command.search.arguments.all: all
	command.search.arguments.id: id
	command.search.arguments.categories: categories
	command.search.arguments.name: name
	command.search.arguments.lore: lore
	command.search.arguments.player: player
	command.select: *id015
	command.select.aliases: *id016
	command.select.description: 'Same args as purge, but it show the info instead on remove:
	  http://marketplacedocs.readthedocs.io/en/latest/commands/purge.html'
	command.select.argumentsHelp: <argument-name> [argument-value]...
	command.limits: *id017
	command.limits.aliases: *id018
	command.limits.description: Manage player limits
	command.limits.argumentsHelp: <set|get|increment|decrement> <player> [slots]
	command.reload: *id019
	command.reload.aliases: *id020
	command.reload.description: Reload configuration
	command.reload.argumentsHelp: ''
	command.help: *id021
	command.help.aliases: *id022
	command.help.description: Display this menu
	command.help.argumentsHelp: ''
	command.setpin: *id023
	command.setpin.aliases: *id024
	command.setpin.description: Set the pin for login through the web client
	command.setpin.argumentsHelp: <new-pin>
	command.cancel: *id025
	command.cancel.aliases: *id026
	command.cancel.description: Cancel all the listings (this is an experimental/migration command)
	command.cancel.argumentsHelp: --all
	command.wallet: *id027
	command.wallet.aliases: *id028
	command.wallet.description: Adds money to your web account, this allows you yo purchase items through the web system
	command.wallet.argumentsHelp: <deposit|withdraw|check> [player|amount] [amount]
	command.wallet.arguments: *id029
	command.wallet.arguments.deposit: deposit
	command.wallet.arguments.withdraw: withdraw
	command.wallet.arguments.check: check
	database:
	  mysql: &id030
	    hostname: localhost
	    username: root
	    password: '123'
	    port: '3306'
	    database: marketplace
	  sqlite: &id031
	    file: marketplace.db
	  type: sqlite
	  tables: &id032
	    catalog: catalog
	    limit: limit
	    webaccounts: webaccounts
	    sync_info: syncinfo
	database.mysql: *id030
	database.mysql.hostname: localhost
	database.mysql.username: root
	database.mysql.password: '123'
	database.mysql.port: '3306'
	database.mysql.database: marketplace
	database.sqlite: *id031
	database.sqlite.file: marketplace.db
	database.type: sqlite
	database.tables: *id032
	database.tables.catalog: catalog
	database.tables.limit: limit
	database.tables.webaccounts: webaccounts
	database.tables.sync_info: syncinfo
	webmarket:
	  enabled: false
	  pin: &id033
	    empty: '&cPlease insert a pin (All web sessions have been closed)'
	    done: '&aYour pin has been established'
	    error: '&cUnexpected error while changing your pin, please contact an administrator'
	  account: &id034
	    invalid: '&cSorry but this account doesn''t exists, please use /mp setpin <pin>
	      to set a pin and create the account'
	    money: '&7Wallet Money:&6 {money}$'
	    deposit: '&aYou just deposited &6${money}&a in your wallet'
	    withdraw: '&aYou just withdraw &6${money}&a from your wallet'
	    error: '&cUnexpected error while modifying your account data, please contact an
	      administrator'
	    allow_withdraw: true
	webmarket.enabled: false
	webmarket.pin: *id033
	webmarket.pin.empty: '&cPlease insert a pin (All web sessions have been closed)'
	webmarket.pin.done: '&aYour pin has been established'
	webmarket.pin.error: '&cUnexpected error while changing your pin, please contact an
	  administrator'
	webmarket.account: *id034
	webmarket.account.invalid: '&cSorry but this account doesn''t exists, please use /mp
	  setpin <pin> to set a pin and create the account'
	webmarket.account.money: '&7Wallet Money:&6 {money}$'
	webmarket.account.deposit: '&aYou just deposited &6${money}&a in your wallet'
	webmarket.account.withdraw: '&aYou just withdraw &6${money}&a from your wallet'
	webmarket.account.error: '&cUnexpected error while modifying your account data, please
	  contact an administrator'
	webmarket.account.allow_withdraw: true
	limits:
	  default: -1
	  reach: '&cYou reach the limit of &6{number}&c listings at the same time!'
	  mode: permissions
	  multiple: stack
	  permissions: &id035
	  - marketplace.limits.vip=3
	  - marketplace.limits.donor=2
	limits.default: -1
	limits.reach: '&cYou reach the limit of &6{number}&c listings at the same time!'
	limits.mode: permissions
	limits.multiple: stack
	limits.permissions: *id035
	logs:
	  console: true
	  file: true
	  publish: true
	  remove_listing: true
	  claim: true
	  purchase: true
	logs.console: true
	logs.file: true
	logs.publish: true
	logs.remove_listing: true
	logs.claim: true
	logs.purchase: true
	publish:
	  price: &id036
	    min: 1
	    max: 2000000000
	    error: '&cThat price is out of bounds!'
	  invaliditem: '&cInvalid item'
	  done: '&aYou publish &6{item} &afor &7${price}&a into the marketplace'
	  claim: '&aYou claim &6${price}&a from &6{item}'
	  bulkclaim: '&aYou claimed the money of &6{amount}&a sold items and got &6{price}$'
	  bulkclaim_enabled: true
	  error: '&cUnexpected error ocurred while publising your item, please contact to
	    server administrator with the current time'
	publish.price: *id036
	publish.price.min: 1
	publish.price.max: 2000000000
	publish.price.error: '&cThat price is out of bounds!'
	publish.invaliditem: '&cInvalid item'
	publish.done: '&aYou publish &6{item} &afor &7${price}&a into the marketplace'
	publish.claim: '&aYou claim &6${price}&a from &6{item}'
	publish.bulkclaim: '&aYou claimed the money of &6{amount}&a sold items and got &6{price}$'
	publish.bulkclaim_enabled: true
	publish.error: '&cUnexpected error ocurred while publising your item, please contact
	  to server administrator with the current time'
	messages:
	  header: '&6[&dMarket&bPlace&6]&7 '
	  invalidnumber: '&cInvalid number'
	  invalidplayer: '&cInvalid player'
	  dropped: '&eSome items have been dropped!'
	messages.header: '&6[&dMarket&bPlace&6]&7 '
	messages.invalidnumber: '&cInvalid number'
	messages.invalidplayer: '&cInvalid player'
	messages.dropped: '&eSome items have been dropped!'
	menu:
	  nextpage: '&7Next page'
	  previouspage: '&7Previous page'
	  page: &id037
	    title: '&7Page: &6{page}/{pages}'
	    lore: &id038
	    - '&6{items}&7 item/s'
	  marketplace: &id039
	    title: '&9MarketPlace (&6{search}&9)'
	    filters: &id040
	      title: '&7Filters...'
	    item: &id041
	    - '&6---------'
	    - '&dSeller: &6{seller}'
	    - '&cPublished: &6{published}'
	    - '&9Expires: &6{expires}'
	    - '&7Price: &6${price}'
	    - '&8Per Item: &6${per_item}'
	    - '&3Buyer Tax: &6${tax} &7({percent}%)'
	    - '&aTotal: &6${total}'
	    back: '&bBack'
	    loading: '&6Loading...'
	    gotomy: '&6Go to Your Listings'
	    reference: &id042
	      ingame: '&6In-Game'
	      webmarket: '&3Web'
	    order: &id043
	      price: &id044
	        name: '&7Order By: &6Price'
	        asc: '&3Cheap to expensive'
	        desc: '&3Expensive to cheap'
	      item_amount: &id045
	        name: '&7Order By: &7Amount'
	        asc: '&3Less to more'
	        desc: '&3More to less'
	      publish_date: &id046
	        name: '&7Order By: &2Time'
	        asc: '&3Older to newer'
	        desc: '&3Newer to older'
	    claimall: '&6Claim All'
	    asc: '&3Ascending'
	    desc: '&3Descending'
	  main: &id047
	    title: '&9MarketPlace'
	    idsearch: '&eSearch By ID'
	    namesearch: '&eSearch By Name'
	    loresearch: '&eSearch By Lore'
	    allsearch: '&eSearch all MarketPlace'
	    categories: '&eSearch Categories'
	  categories: &id048
	    title: '&eSelect a category'
	  listings: &id049
	    deliveries: '&5Deliveries ({amount})'
	    gotosearch: '&7Go to Search Menu'
	    unclaimed: '&dWaiting for money claim'
	    unbought: '&cUnbought listings'
	    cancelled: '&cCancelled/Expired listings'
	    removed: '&aYou remove succesfully your listing &6{listing}!'
	    history: &id050
	      purchases: '&3Purchases History'
	      purchasesLore: &id051
	      - '&6---------'
	      - '&7Price:&6 ${price}'
	      - '&7Seller:&6 {seller}'
	      - '&7Published:&6 {published}'
	      - '&7Purchased:&6 {purchased}'
	      - '&7Purchased at:&6 {reference}'
	      sales: '&9Sales History'
	      salesLore: &id052
	      - '&6---------'
	      - '&7Price:&6 ${price}'
	      - '&7Buyer:&6 {buyer}'
	      - '&7Published:&6 {published}'
	      - '&7Purchased:&6 {purchased}'
	    claims: &id053
	      title: '&9Claim menu'
	      claimlore: &id054
	      - '&6---------'
	      - '&7Earning:&6 ${price}'
	      - '&7Seller Tax:&6 ${tax} &7({percent}%)'
	      - '&7Total: &6{total}'
	      - '&7Buyer:&6 {buyer}'
	      - '&7Bought:&6 {bought}'
	      - '&7Published:&6 {published}'
	      - '&7Purchased at:&6 {reference}'
	  deliveries: &id055
	    claimed: '&7You claimed a delivery!'
	    lore: &id056
	    - '&6---------'
	    - '&7Price:&6 ${price}'
	    - '&7Seller:&6 {seller}'
	    - '&7Published:&6 {published}'
	    - '&7Purchased:&6 {purchased}'
	    title: '&6Your deliveries'
	  confirm: &id057
	    title: '&aConfirm Purchase'
	    cancel: '&cCancel'
	    seller: '&7Seller:&6 {seller}'
	    price: '&7Price:&6 ${price}'
	    confirm: &id058
	      name: '&aPurchase'
	      lore: &id059
	      - '&7Your money:&6 ${money}'
	      - '&7After Purchase:&6 ${money-after}'
	  idsearch: &id060
	    title: '&3Search By ID'
	    info: &id061
	    - '&dClick to search &6{name}&d in MarketPlace'
	  my: &id062
	    title: '&5My Listings'
	  items: &id063
	    background: &id064
	      item: STAINED_GLASS_PANE
	      subid: 7
	      name: '&0'
	    changemenu: &id065
	      item: ARROW
	    purchasesHistory: &id066
	      item: ENCHANTED_BOOK
	    unbought: &id067
	      item: NAME_TAG
	    deliveries: &id068
	      item: MINECART
	    cancelled: &id069
	      item: BARRIER
	    salesHistory: &id070
	      item: BOOK
	    claimNormal: &id071
	      item: GOLDEN_APPLE
	    claimNotification: &id072
	      item: GOLDEN_APPLE
	      subid: 1
	    searchName: &id073
	      item: NAME_TAG
	    searchID: &id074
	      item: APPLE
	    searchCategories: &id075
	      item: BOOKSHELF
	    searchLore: &id076
	      item: BOOK
	    searchAll: &id077
	      item: GOLDEN_APPLE
	    back: &id078
	      item: REDSTONE
	    confirmCancel: &id079
	      item: REDSTONE_BLOCK
	    confirmPurchase: &id080
	      item: WOOL
	      subid: 5
	    page: &id081
	      item: FEATHER
	    pageNext: &id082
	      item: ARROW
	    pageBack: &id083
	      item: ARROW
	    priceOrder: &id084
	      item: ARROW
	    amountOrder: &id085
	      item: COBBLESTONE
	    timeOrder: &id086
	      item: WATCH
	    claimAll: &id087
	      item: GOLDEN_APPLE
	menu.nextpage: '&7Next page'
	menu.previouspage: '&7Previous page'
	menu.page: *id037
	menu.page.title: '&7Page: &6{page}/{pages}'
	menu.page.lore: *id038
	menu.marketplace: *id039
	menu.marketplace.title: '&9MarketPlace (&6{search}&9)'
	menu.marketplace.filters: *id040
	menu.marketplace.filters.title: '&7Filters...'
	menu.marketplace.item: *id041
	menu.marketplace.back: '&bBack'
	menu.marketplace.loading: '&6Loading...'
	menu.marketplace.gotomy: '&6Go to Your Listings'
	menu.marketplace.reference: *id042
	menu.marketplace.reference.ingame: '&6In-Game'
	menu.marketplace.reference.webmarket: '&3Web'
	menu.marketplace.order: *id043
	menu.marketplace.order.price: *id044
	menu.marketplace.order.price.name: '&7Order By: &6Price'
	menu.marketplace.order.price.asc: '&3Cheap to expensive'
	menu.marketplace.order.price.desc: '&3Expensive to cheap'
	menu.marketplace.order.item_amount: *id045
	menu.marketplace.order.item_amount.name: '&7Order By: &7Amount'
	menu.marketplace.order.item_amount.asc: '&3Less to more'
	menu.marketplace.order.item_amount.desc: '&3More to less'
	menu.marketplace.order.publish_date: *id046
	menu.marketplace.order.publish_date.name: '&7Order By: &2Time'
	menu.marketplace.order.publish_date.asc: '&3Older to newer'
	menu.marketplace.order.publish_date.desc: '&3Newer to older'
	menu.marketplace.claimall: '&6Claim All'
	menu.marketplace.asc: '&3Ascending'
	menu.marketplace.desc: '&3Descending'
	menu.main: *id047
	menu.main.title: '&9MarketPlace'
	menu.main.idsearch: '&eSearch By ID'
	menu.main.namesearch: '&eSearch By Name'
	menu.main.loresearch: '&eSearch By Lore'
	menu.main.allsearch: '&eSearch all MarketPlace'
	menu.main.categories: '&eSearch Categories'
	menu.categories: *id048
	menu.categories.title: '&eSelect a category'
	menu.listings: *id049
	menu.listings.deliveries: '&5Deliveries ({amount})'
	menu.listings.gotosearch: '&7Go to Search Menu'
	menu.listings.unclaimed: '&dWaiting for money claim'
	menu.listings.unbought: '&cUnbought listings'
	menu.listings.cancelled: '&cCancelled/Expired listings'
	menu.listings.removed: '&aYou remove succesfully your listing &6{listing}!'
	menu.listings.history: *id050
	menu.listings.history.purchases: '&3Purchases History'
	menu.listings.history.purchasesLore: *id051
	menu.listings.history.sales: '&9Sales History'
	menu.listings.history.salesLore: *id052
	menu.listings.claims: *id053
	menu.listings.claims.title: '&9Claim menu'
	menu.listings.claims.claimlore: *id054
	menu.deliveries: *id055
	menu.deliveries.claimed: '&7You claimed a delivery!'
	menu.deliveries.lore: *id056
	menu.deliveries.title: '&6Your deliveries'
	menu.confirm: *id057
	menu.confirm.title: '&aConfirm Purchase'
	menu.confirm.cancel: '&cCancel'
	menu.confirm.seller: '&7Seller:&6 {seller}'
	menu.confirm.price: '&7Price:&6 ${price}'
	menu.confirm.confirm: *id058
	menu.confirm.confirm.name: '&aPurchase'
	menu.confirm.confirm.lore: *id059
	menu.idsearch: *id060
	menu.idsearch.title: '&3Search By ID'
	menu.idsearch.info: *id061
	menu.my: *id062
	menu.my.title: '&5My Listings'
	menu.items: *id063
	menu.items.background: *id064
	menu.items.background.item: STAINED_GLASS_PANE
	menu.items.background.subid: 7
	menu.items.background.name: '&0'
	menu.items.changemenu: *id065
	menu.items.changemenu.item: ARROW
	menu.items.purchasesHistory: *id066
	menu.items.purchasesHistory.item: ENCHANTED_BOOK
	menu.items.unbought: *id067
	menu.items.unbought.item: NAME_TAG
	menu.items.deliveries: *id068
	menu.items.deliveries.item: MINECART
	menu.items.cancelled: *id069
	menu.items.cancelled.item: BARRIER
	menu.items.salesHistory: *id070
	menu.items.salesHistory.item: BOOK
	menu.items.claimNormal: *id071
	menu.items.claimNormal.item: GOLDEN_APPLE
	menu.items.claimNotification: *id072
	menu.items.claimNotification.item: GOLDEN_APPLE
	menu.items.claimNotification.subid: 1
	menu.items.searchName: *id073
	menu.items.searchName.item: NAME_TAG
	menu.items.searchID: *id074
	menu.items.searchID.item: APPLE
	menu.items.searchCategories: *id075
	menu.items.searchCategories.item: BOOKSHELF
	menu.items.searchLore: *id076
	menu.items.searchLore.item: BOOK
	menu.items.searchAll: *id077
	menu.items.searchAll.item: GOLDEN_APPLE
	menu.items.back: *id078
	menu.items.back.item: REDSTONE
	menu.items.confirmCancel: *id079
	menu.items.confirmCancel.item: REDSTONE_BLOCK
	menu.items.confirmPurchase: *id080
	menu.items.confirmPurchase.item: WOOL
	menu.items.confirmPurchase.subid: 5
	menu.items.page: *id081
	menu.items.page.item: FEATHER
	menu.items.pageNext: *id082
	menu.items.pageNext.item: ARROW
	menu.items.pageBack: *id083
	menu.items.pageBack.item: ARROW
	menu.items.priceOrder: *id084
	menu.items.priceOrder.item: ARROW
	menu.items.amountOrder: *id085
	menu.items.amountOrder.item: COBBLESTONE
	menu.items.timeOrder: *id086
	menu.items.timeOrder.item: WATCH
	menu.items.claimAll: *id087
	menu.items.claimAll.item: GOLDEN_APPLE
	misc:
	  disabled: '&cThis feature is currently disabled!'
	  nomoney: '&cYou don''t have money to perform this action'
	misc.disabled: '&cThis feature is currently disabled!'
	misc.nomoney: '&cYou don''t have money to perform this action'
	searches:
	  categories: false
	  name: true
	  id: true
	  lore: true
	searches.categories: false
	searches.name: true
	searches.id: true
	searches.lore: true
	categories:
	  tools: &id088
	    name: '&bTools'
	    icon: WOOD_PICKAXE
	    description: '&7Axes, Pickxes, Hoes and more tools!'
	    items: &id089
	    - FLINT_AND_STEEL
	    - COMPASS
	    - WATCH
	    - FISHING_ROD
	    - SHEARS
	    - LEASH
	    - WOOD_HOE
	    - STONE_HOE
	    - IRON_HOE
	    - DIAMOND_HOE
	    - GOLD_HOE
	    - WOOD_AXE
	    - STONE_AXE
	    - IRON_AXE
	    - DIAMOND_AXE
	    - GOLD_AXE
	    - WOOD_PICKAXE
	    - STONE_PICKAXE
	    - IRON_PICKAXE
	    - DIAMOND_PICKAXE
	    - GOLD_PICKAXE
	  equipment: &id090
	    name: '&5Equipment'
	    icon: IRON_HELMET
	    description: '&7Armors of any kind'
	    items: &id091
	    - LEATHER_HELMET
	    - LEATHER_CHESTPLATE
	    - LEATHER_LEGGINGS
	    - LEATHER_BOOTS
	    - CHAINMAIL_HELMET
	    - CHAINMAIL_CHESTPLATE
	    - CHAINMAIL_LEGGINGS
	    - CHAINMAIL_BOOTS
	    - IRON_HELMET
	    - IRON_CHESTPLATE
	    - IRON_LEGGINGS
	    - IRON_BOOTS
	    - DIAMOND_HELMET
	    - DIAMOND_CHESTPLATE
	    - DIAMOND_LEGGINGS
	    - DIAMOND_BOOTS
	    - GOLD_HELMET
	    - GOLD_CHESTPLATE
	    - GOLD_LEGGINGS
	    - GOLD_BOOTS
	  blocks: &id092
	    name: '&7Blocks'
	    icon: DIRT
	    description: '&bAll the blocks you can imagine'
	    items: &id093
	    - AIR
	    - STONE
	    - GRASS
	    - DIRT
	    - COBBLESTONE
	    - WOOD
	    - SAPLING
	    - BEDROCK
	    - WATER
	    - STATIONARY_WATER
	    - LAVA
	    - STATIONARY_LAVA
	    - SAND
	    - GRAVEL
	    - GOLD_ORE
	    - IRON_ORE
	    - COAL_ORE
	    - LOG
	    - LEAVES
	    - SPONGE
	    - GLASS
	    - LAPIS_ORE
	    - LAPIS_BLOCK
	    - DISPENSER
	    - SANDSTONE
	    - NOTE_BLOCK
	    - BED_BLOCK
	    - POWERED_RAIL
	    - DETECTOR_RAIL
	    - PISTON_STICKY_BASE
	    - WEB
	    - LONG_GRASS
	    - DEAD_BUSH
	    - PISTON_BASE
	    - PISTON_EXTENSION
	    - WOOL
	    - PISTON_MOVING_PIECE
	    - YELLOW_FLOWER
	    - RED_ROSE
	    - BROWN_MUSHROOM
	    - RED_MUSHROOM
	    - GOLD_BLOCK
	    - IRON_BLOCK
	    - DOUBLE_STEP
	    - STEP
	    - BRICK
	    - TNT
	    - BOOKSHELF
	    - MOSSY_COBBLESTONE
	    - OBSIDIAN
	    - TORCH
	    - FIRE
	    - MOB_SPAWNER
	    - WOOD_STAIRS
	    - CHEST
	    - REDSTONE_WIRE
	    - DIAMOND_ORE
	    - DIAMOND_BLOCK
	    - WORKBENCH
	    - CROPS
	    - SOIL
	    - FURNACE
	    - BURNING_FURNACE
	    - SIGN_POST
	    - WOODEN_DOOR
	    - LADDER
	    - RAILS
	    - COBBLESTONE_STAIRS
	    - WALL_SIGN
	    - LEVER
	    - STONE_PLATE
	    - IRON_DOOR_BLOCK
	    - WOOD_PLATE
	    - REDSTONE_ORE
	    - GLOWING_REDSTONE_ORE
	    - REDSTONE_TORCH_OFF
	    - REDSTONE_TORCH_ON
	    - STONE_BUTTON
	    - SNOW
	    - ICE
	    - SNOW_BLOCK
	    - CACTUS
	    - CLAY
	    - SUGAR_CANE_BLOCK
	    - JUKEBOX
	    - FENCE
	    - PUMPKIN
	    - NETHERRACK
	    - SOUL_SAND
	    - GLOWSTONE
	    - PORTAL
	    - JACK_O_LANTERN
	    - CAKE_BLOCK
	    - DIODE_BLOCK_OFF
	    - DIODE_BLOCK_ON
	    - STAINED_GLASS
	    - TRAP_DOOR
	    - MONSTER_EGGS
	    - SMOOTH_BRICK
	    - HUGE_MUSHROOM_1
	    - HUGE_MUSHROOM_2
	    - IRON_FENCE
	    - THIN_GLASS
	    - MELON_BLOCK
	    - PUMPKIN_STEM
	    - MELON_STEM
	    - VINE
	    - FENCE_GATE
	    - BRICK_STAIRS
	    - SMOOTH_STAIRS
	    - MYCEL
	    - WATER_LILY
	    - NETHER_BRICK
	    - NETHER_FENCE
	    - NETHER_BRICK_STAIRS
	    - NETHER_WARTS
	    - ENCHANTMENT_TABLE
	    - BREWING_STAND
	    - CAULDRON
	    - ENDER_PORTAL
	    - ENDER_PORTAL_FRAME
	    - ENDER_STONE
	    - DRAGON_EGG
	    - REDSTONE_LAMP_OFF
	    - REDSTONE_LAMP_ON
	    - WOOD_DOUBLE_STEP
	    - WOOD_STEP
	    - COCOA
	    - SANDSTONE_STAIRS
	    - EMERALD_ORE
	    - ENDER_CHEST
	    - TRIPWIRE_HOOK
	    - TRIPWIRE
	    - EMERALD_BLOCK
	    - SPRUCE_WOOD_STAIRS
	    - BIRCH_WOOD_STAIRS
	    - JUNGLE_WOOD_STAIRS
	    - COMMAND
	    - BEACON
	    - COBBLE_WALL
	    - FLOWER_POT
	    - CARROT
	    - POTATO
	    - WOOD_BUTTON
	    - SKULL
	    - ANVIL
	    - TRAPPED_CHEST
	    - GOLD_PLATE
	    - IRON_PLATE
	    - REDSTONE_COMPARATOR_OFF
	    - REDSTONE_COMPARATOR_ON
	    - DAYLIGHT_DETECTOR
	    - REDSTONE_BLOCK
	    - QUARTZ_ORE
	    - HOPPER
	    - QUARTZ_BLOCK
	    - QUARTZ_STAIRS
	    - ACTIVATOR_RAIL
	    - DROPPER
	    - STAINED_CLAY
	    - STAINED_GLASS_PANE
	    - LEAVES_2
	    - LOG_2
	    - ACACIA_STAIRS
	    - DARK_OAK_STAIRS
	    - SLIME_BLOCK
	    - BARRIER
	    - IRON_TRAPDOOR
	    - PRISMARINE
	    - SEA_LANTERN
	    - HAY_BLOCK
	    - CARPET
	    - HARD_CLAY
	    - COAL_BLOCK
	    - PACKED_ICE
	    - DOUBLE_PLANT
	    - STANDING_BANNER
	    - WALL_BANNER
	    - DAYLIGHT_DETECTOR_INVERTED
	    - RED_SANDSTONE
	    - RED_SANDSTONE_STAIRS
	    - DOUBLE_STONE_SLAB2
	    - STONE_SLAB2
	    - SPRUCE_FENCE_GATE
	    - BIRCH_FENCE_GATE
	    - JUNGLE_FENCE_GATE
	    - DARK_OAK_FENCE_GATE
	    - ACACIA_FENCE_GATE
	    - SPRUCE_FENCE
	    - BIRCH_FENCE
	    - JUNGLE_FENCE
	    - DARK_OAK_FENCE
	    - ACACIA_FENCE
	    - SPRUCE_DOOR
	    - BIRCH_DOOR
	    - JUNGLE_DOOR
	    - ACACIA_DOOR
	    - DARK_OAK_DOOR
	  weapons: &id094
	    name: '&6Weapons'
	    icon: STONE_SWORD
	    description: '&7Swords, bows and arrows'
	    items: &id095
	    - BOW
	    - ARROW
	    - SPECTRAL_ARROW
	    - TIPPED_ARROW
	    - WOOD_SWORD
	    - STONE_SWORD
	    - IRON_SWORD
	    - DIAMOND_SWORD
	    - GOLD_SWORD
	  redstone: &id096
	    name: '&cRedstone'
	    icon: REDSTONE
	    description: '&7Everything you need to\n&7create redstone contraptions'
	    items: &id097
	    - REDSTONE
	    - DIODE
	    - REDSTONE_COMPARATOR
	    - REDSTONE_TORCH_ON
	    - DISPENSER
	    - DROPPER
	    - HOPPER
	    - LEVER
	    - REDSTONE_LAMP_OFF
	    - TRIPWIRE_HOOK
	    - NOTE_BLOCK
	    - PISTON_STICKY_BASE
	    - PISTON_BASE
	    - TNT
	    - DAYLIGHT_DETECTOR
	    - STONE_BUTTON
	    - WOOD_BUTTON
	    - TRAP_DOOR
	    - IRON_TRAPDOOR
	    - STONE_PLATE
	    - WOOD_PLATE
	    - GOLD_PLATE
	    - IRON_PLATE
	categories.tools: *id088
	categories.tools.name: '&bTools'
	categories.tools.icon: WOOD_PICKAXE
	categories.tools.description: '&7Axes, Pickxes, Hoes and more tools!'
	categories.tools.items: *id089
	categories.equipment: *id090
	categories.equipment.name: '&5Equipment'
	categories.equipment.icon: IRON_HELMET
	categories.equipment.description: '&7Armors of any kind'
	categories.equipment.items: *id091
	categories.blocks: *id092
	categories.blocks.name: '&7Blocks'
	categories.blocks.icon: DIRT
	categories.blocks.description: '&bAll the blocks you can imagine'
	categories.blocks.items: *id093
	categories.weapons: *id094
	categories.weapons.name: '&6Weapons'
	categories.weapons.icon: STONE_SWORD
	categories.weapons.description: '&7Swords, bows and arrows'
	categories.weapons.items: *id095
	categories.redstone: *id096
	categories.redstone.name: '&cRedstone'
	categories.redstone.icon: REDSTONE
	categories.redstone.description: '&7Everything you need to\n&7create redstone contraptions'
	categories.redstone.items: *id097
	chatsearch:
	  lore: '&aWrite in chat the lore you want to search (- to cancel):'
	  name: '&aWrite in chat the name you want to search (- to cancel):'
	  cancel: '-'
	  cancelled: '&cSearch cancelled'
	  timeout_seconds: 60
	chatsearch.lore: '&aWrite in chat the lore you want to search (- to cancel):'
	chatsearch.name: '&aWrite in chat the name you want to search (- to cancel):'
	chatsearch.cancel: '-'
	chatsearch.cancelled: '&cSearch cancelled'
	chatsearch.timeout_seconds: 60
	purchase:
	  nomoney: '&cYou don''t have money to purchase this item!'
	  noavailable: '&cSorry, this item is no longer available'
	  purchase: '&aYou purchase &6{item}&a successfully'
	  notification: '&6{buyer}&a buy your &6{item}&a claim your money in &7/market my'
	  notificationJoin: '&aYou have &6{listings}&a listings to claim (Use &7/market my&a
	    to claim it)!'
	purchase.nomoney: '&cYou don''t have money to purchase this item!'
	purchase.noavailable: '&cSorry, this item is no longer available'
	purchase.purchase: '&aYou purchase &6{item}&a successfully'
	purchase.notification: '&6{buyer}&a buy your &6{item}&a claim your money in &7/market
	  my'
	purchase.notificationJoin: '&aYou have &6{listings}&a listings to claim (Use &7/market
	  my&a to claim it)!'
	shout:
	  permission: market.shout
	  message: '&6{player}&3 published &6{item}&3 in the marketplace'
	  click: '&7[Click here to open {player}''s shop]'
	shout.permission: market.shout
	shout.message: '&6{player}&3 published &6{item}&3 in the marketplace'
	shout.click: '&7[Click here to open {player}''s shop]'
	date:
	  format: dd/MM/yy
	  now: just now
	  seconds: '{time} seconds ago'
	  minutes: '{time} minutes ago'
	  never: Never
	date.format: dd/MM/yy
	date.now: just now
	date.seconds: '{time} seconds ago'
	date.minutes: '{time} minutes ago'
	date.never: Never
	money:
	  format: '#,###.00'
	  formatLocale: en-US
	money.format: '#,###.00'
	money.formatLocale: en-US
	tax:
	  sellerTax: 1.35
	  buyerTax: 0
	  webPurchaseTax: 0.0
	  publish: &id098
	    permissions: &id099
	    - market.publish_tax.vip=4
	    default: 0.0
	    confirm: '&cBy publishing this item ${money} (A {tax}% of the raw price) will
	      be withdrawn from your account, please type this command again to confirm'
	    confirm_cancel: '&cPublish confirm cancelled'
	    confirm_time: 5
	    nomoney: '&cSorry but you have not enough money to pay publish taxes (${money})'
	    return_on_cancel: false
	    return_on_cancel_expired: false
	    return_message: '&a${amount} has been deposited to your account'
	tax.sellerTax: 1.35
	tax.buyerTax: 0
	tax.webPurchaseTax: 0.0
	tax.publish: *id098
	tax.publish.permissions: *id099
	tax.publish.default: 0.0
	tax.publish.confirm: '&cBy publishing this item ${money} (A {tax}% of the raw price)
	  will be withdrawn from your account, please type this command again to confirm'
	tax.publish.confirm_cancel: '&cPublish confirm cancelled'
	tax.publish.confirm_time: 5
	tax.publish.nomoney: '&cSorry but you have not enough money to pay publish taxes (${money})'
	tax.publish.return_on_cancel: false
	tax.publish.return_on_cancel_expired: false
	tax.publish.return_message: '&a${amount} has been deposited to your account'
	timeout:
	  default: 7d
	  permissions: &id100
	  - market.timeout.vip=30d
	  - market.timeout.never=infinite
	timeout.default: 7d
	timeout.permissions: *id100
	placeholderapi:
	  latest: '&6{item} &c{price}$ &7({seller})'
	placeholderapi.latest: '&6{item} &c{price}$ &7({seller})'
	langutils:
	  default: en_us
	langutils.default: en_us
	blacklist:
	  enabled: false
	  message: '&cYou cannot publish this item in the market!'
	  items: &id101
	  - DRAGON_EGG
	  lore_enabled: false
	  lores: &id102
	  - Special Item
	  name_enabled: false
	  names: &id103
	  - Super Item
	blacklist.enabled: false
	blacklist.message: '&cYou cannot publish this item in the market!'
	blacklist.items: *id101
	blacklist.lore_enabled: false
	blacklist.lores: *id102
	blacklist.name_enabled: false
	blacklist.names: *id103
	discordWebhook:
	  enabled: false
	  debug: false
	  url: ''
	  botName: MarketPlace
	  botAvatar: https://www.spigotmc.org/data/resource_icons/48/48526.jpg
	  notification: &id104
	    publish: &id105
	      enabled: true
	      title: New Item Published
	      description: '**{player}** published **{item}** for **${price}**'
	      color: '#fec601'
	    purchase: &id106
	      enabled: true
	      title: Item Purchased
	      description: '**{buyer}** purchased **{item}** for **${price}** published by
	        **{seller}**'
	      color: '#30e539'
	discordWebhook.enabled: false
	discordWebhook.debug: false
	discordWebhook.url: ''
	discordWebhook.botName: MarketPlace
	discordWebhook.botAvatar: https://www.spigotmc.org/data/resource_icons/48/48526.jpg
	discordWebhook.notification: *id104
	discordWebhook.notification.publish: *id105
	discordWebhook.notification.publish.enabled: true
	discordWebhook.notification.publish.title: New Item Published
	discordWebhook.notification.publish.description: '**{player}** published **{item}**
	  for **${price}**'
	discordWebhook.notification.publish.color: '#fec601'
	discordWebhook.notification.purchase: *id106
	discordWebhook.notification.purchase.enabled: true
	discordWebhook.notification.purchase.title: Item Purchased
	discordWebhook.notification.purchase.description: '**{buyer}** purchased **{item}**
	  for **${price}** published by **{seller}**'
	discordWebhook.notification.purchase.color: '#30e539'
	

~~~~~
Table
~~~~~


+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| Configuration Node                                      | Type                    | Default                                                                                                                                       | Help                                                                                                                                                |
+=========================================================+=========================+===============================================================================================================================================+=====================================================================================================================================================+
| :doc:`allowPublish`                                     | Boolean (true or false) | true                                                                                                                                          | Disallow players from publish items                                                                                                                 |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`commands.skiphelp`                                | Boolean (true or false) | false                                                                                                                                         | If true /marketplace command will skip help message and instead open make the same function as /marketplace search                                  |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`commands.help`                                    | String                  | &a/market &c{name} &3{arguments} &6(&7{help}&6)                                                                                               | Commands help format                                                                                                                                |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`commands.show-default-aliases`                    | Boolean (true or false) | true                                                                                                                                          | If true, help command will display the default subcommands                                                                                          |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.aliases`                                  | String list             | This is a list, click on the name to see it                                                                                                   | You have to restart the server to apply the changes                                                                                                 |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.marketall.aliases`                        | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.marketall.permission`                     | String                  | none                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`commands.nopermission`                            | String                  | &cYou don't permission to use this command                                                                                                    |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.my.aliases`                               | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.my.description`                           | String                  | Check your sold, unsold, history etc                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.my.argumentsHelp`                         | String                  |                                                                                                                                               |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.listings.aliases`                         | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.listings.description`                     | String                  | Open the menu of unbrought items of any player (You can remove listings)                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.listings.argumentsHelp`                   | String                  | <player_name|player_uuid>                                                                                                                     |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.publish.aliases`                          | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.publish.description`                      | String                  | Publish a item in the marketplace                                                                                                             |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.publish.argumentsHelp`                    | String                  | <price>                                                                                                                                       |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.purge.aliases`                            | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.purge.description`                        | String                  | Before use this command make sure you read this: http://marketplacedocs.readthedocs.io/en/latest/commands/purge.html                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.purge.argumentsHelp`                      | String                  | <argument-name> [argument-value]                                                                                                              |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.search.aliases`                           | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.search.description`                       | String                  | Open the search menu                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.search.argumentsHelp`                     | String                  | [all|id|categories|name|lore|player] [name|lore|player-name]                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.search.arguments.all`                     | String                  | all                                                                                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.search.arguments.id`                      | String                  | id                                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.search.arguments.categories`              | String                  | categories                                                                                                                                    |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.search.arguments.name`                    | String                  | name                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.search.arguments.lore`                    | String                  | lore                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.search.arguments.player`                  | String                  | player                                                                                                                                        |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.select.aliases`                           | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.select.description`                       | String                  | Same args as purge, but it show the info instead on remove: http://marketplacedocs.readthedocs.io/en/latest/commands/purge.html               |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.select.argumentsHelp`                     | String                  | <argument-name> [argument-value]...                                                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.limits.aliases`                           | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.limits.description`                       | String                  | Manage player limits                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.limits.argumentsHelp`                     | String                  | <set|get|increment|decrement> <player> [slots]                                                                                                |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.reload.aliases`                           | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.reload.description`                       | String                  | Reload configuration                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.reload.argumentsHelp`                     | String                  |                                                                                                                                               |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.help.aliases`                             | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.help.description`                         | String                  | Display this menu                                                                                                                             |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.help.argumentsHelp`                       | String                  |                                                                                                                                               |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.setpin.aliases`                           | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.setpin.description`                       | String                  | Set the pin for login through the web client                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.setpin.argumentsHelp`                     | String                  | <new-pin>                                                                                                                                     |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.cancel.aliases`                           | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.cancel.description`                       | String                  | Cancel all the listings (this is an experimental/migration command)                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.cancel.argumentsHelp`                     | String                  | --all                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.wallet.aliases`                           | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.wallet.description`                       | String                  | Adds money to your web account, this allows you yo purchase items through the web system                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.wallet.argumentsHelp`                     | String                  | <deposit|withdraw|check> [player|amount] [amount]                                                                                             |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.wallet.arguments.deposit`                 | String                  | deposit                                                                                                                                       |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.wallet.arguments.withdraw`                | String                  | withdraw                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`command.wallet.arguments.check`                   | String                  | check                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.mysql.hostname`                          | String                  | localhost                                                                                                                                     | Database hostname                                                                                                                                   |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.mysql.username`                          | String                  | root                                                                                                                                          | Database username                                                                                                                                   |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.mysql.password`                          | String                  | 123                                                                                                                                           | Database password                                                                                                                                   |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.mysql.port`                              | String                  | 3306                                                                                                                                          | Database port                                                                                                                                       |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.mysql.database`                          | String                  | marketplace                                                                                                                                   | Database database name                                                                                                                              |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.sqlite.file`                             | String                  | marketplace.db                                                                                                                                | In case of using SQLite, the name of the file                                                                                                       |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.type`                                    | String                  | sqlite                                                                                                                                        | sqlite or mysql (mysql recommended)                                                                                                                 |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.tables.catalog`                          | String                  | catalog                                                                                                                                       | Name of the table where selling items will be saved                                                                                                 |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.tables.limit`                            | String                  | limit                                                                                                                                         | Name of the table where limits will be saved (If db limits system is enabled)                                                                       |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.tables.webaccounts`                      | String                  | webaccounts                                                                                                                                   | Name of the table where web accounts will be saved (If db web market system is enabled)                                                             |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`database.tables.sync_info`                        | String                  | syncinfo                                                                                                                                      | This table will contain info for the webmarket, protocol number, taxes etc                                                                          |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`webmarket.enabled`                                | Boolean (true or false) | false                                                                                                                                         | Purchase, Manage Listings & more through web (Note that you have to enabled mysql db for this to work)                                              |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`webmarket.pin.empty`                              | String                  | &cPlease insert a pin (All web sessions have been closed)                                                                                     | Purchase, Manage Listings & more through web (Note that you have to enabled mysql db for this to work)                                              |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`webmarket.pin.done`                               | String                  | &aYour pin has been established                                                                                                               | Message displayed when a players change pin                                                                                                         |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`webmarket.pin.error`                              | String                  | &cUnexpected error while changing your pin, please contact an administrator                                                                   | Message displayed when an error occurs on pin change procedure                                                                                      |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`webmarket.account.invalid`                        | String                  | &cSorry but this account doesn't exists, please use /mp setpin <pin> to set a pin and create the account                                      | Used mainly by administrators, when they search an invalid user, and by users, when they query their money                                          |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`webmarket.account.money`                          | String                  | &7Wallet Money:&6 {money}$                                                                                                                    | Used mainly by administrators, when they search an invalid user, and by users, when they query their money                                          |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`webmarket.account.deposit`                        | String                  | &aYou just deposited &6${money}&a in your wallet                                                                                              | When player deposit money in their wallet                                                                                                           |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`webmarket.account.withdraw`                       | String                  | &aYou just withdraw &6${money}&a from your wallet                                                                                             | When player withdraw money from their wallet                                                                                                        |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`webmarket.account.error`                          | String                  | &cUnexpected error while modifying your account data, please contact an administrator                                                         | Unexpected error updating the account data                                                                                                          |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`webmarket.account.allow_withdraw`                 | Boolean (true or false) | true                                                                                                                                          | Depending on the context on the server, sometime is not useful to have a simple bank                                                                |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`limits.default`                                   | Integer                 | -1                                                                                                                                            | That means any player will have access to have 3 (Default) items selling at the same time, util you modify it with /market limits (-1 to unlimited) |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`limits.reach`                                     | String                  | &cYou reach the limit of &6{number}&c listings at the same time!                                                                              | When players reach the limit                                                                                                                        |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`limits.mode`                                      | String                  | permissions                                                                                                                                   | More info: http://marketplacedocs.readthedocs.io/en/latest/misc/limits.html                                                                         |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`limits.multiple`                                  | String                  | stack                                                                                                                                         | More info: http://marketplacedocs.readthedocs.io/en/latest/misc/limits.html                                                                         |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`limits.permissions`                               | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`logs.console`                                     | Boolean (true or false) | true                                                                                                                                          | Log marketplace transactions in console?                                                                                                            |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`logs.file`                                        | Boolean (true or false) | true                                                                                                                                          | Log marketplace transactions in plugins/MaketPlace/marketplace.log?                                                                                 |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`logs.publish`                                     | Boolean (true or false) | true                                                                                                                                          | Log /market publish command?                                                                                                                        |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`logs.remove_listing`                              | Boolean (true or false) | true                                                                                                                                          | Log /market my > Unbrought items > Remove an item action?                                                                                           |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`logs.claim`                                       | Boolean (true or false) | true                                                                                                                                          | Log /market my > Waiting for Money Claim > Claim money action?                                                                                      |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`logs.purchase`                                    | Boolean (true or false) | true                                                                                                                                          | Log /market search > Purchase an item action?                                                                                                       |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`publish.price.min`                                | Integer                 | 1                                                                                                                                             | Min price (No recommended less than 1)                                                                                                              |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`publish.price.max`                                | Integer                 | 2000000000                                                                                                                                    | Max price (It may have problems upper 2,000,000,000)                                                                                                |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`publish.price.error`                              | String                  | &cThat price is out of bounds!                                                                                                                | When the price is out of min or max                                                                                                                 |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`publish.invaliditem`                              | String                  | &cInvalid item                                                                                                                                | When the item is air                                                                                                                                |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`publish.done`                                     | String                  | &aYou publish &6{item} &afor &7${price}&a into the marketplace                                                                                | When a item is published                                                                                                                            |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`publish.claim`                                    | String                  | &aYou claim &6${price}&a from &6{item}                                                                                                        | When claim a sold listing                                                                                                                           |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`publish.bulkclaim`                                | String                  | &aYou claimed the money of &6{amount}&a sold items and got &6{price}$                                                                         | When claim all sold listing                                                                                                                         |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`publish.bulkclaim_enabled`                        | Boolean (true or false) | true                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`publish.error`                                    | String                  | &cUnexpected error ocurred while publising your item, please contact to server administrator with the current time                            | When internal stuff fails, you should search the error in console with the hour and report it to rodel77                                            |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`messages.header`                                  | String                  | &6[&dMarket&bPlace&6]&7                                                                                                                       | Header of all messages                                                                                                                              |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`messages.invalidnumber`                           | String                  | &cInvalid number                                                                                                                              | Invalid number                                                                                                                                      |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`messages.invalidplayer`                           | String                  | &cInvalid player                                                                                                                              | Invalid player                                                                                                                                      |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`messages.dropped`                                 | String                  | &eSome items have been dropped!                                                                                                               | When your menu is full and some items got dropped                                                                                                   |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.nextpage`                                    | String                  | &7Next page                                                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.previouspage`                                | String                  | &7Previous page                                                                                                                               |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.page.title`                                  | String                  | &7Page: &6{page}/{pages}                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.page.lore`                                   | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.title`                           | String                  | &9MarketPlace (&6{search}&9)                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.filters.title`                   | String                  | &7Filters...                                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.item`                            | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.back`                            | String                  | &bBack                                                                                                                                        |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.loading`                         | String                  | &6Loading...                                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.gotomy`                          | String                  | &6Go to Your Listings                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.reference.ingame`                | String                  | &6In-Game                                                                                                                                     |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.reference.webmarket`             | String                  | &3Web                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.order.price.name`                | String                  | &7Order By: &6Price                                                                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.order.price.asc`                 | String                  | &3Cheap to expensive                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.order.price.desc`                | String                  | &3Expensive to cheap                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.order.item_amount.name`          | String                  | &7Order By: &7Amount                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.order.item_amount.asc`           | String                  | &3Less to more                                                                                                                                |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.order.item_amount.desc`          | String                  | &3More to less                                                                                                                                |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.order.publish_date.name`         | String                  | &7Order By: &2Time                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.order.publish_date.asc`          | String                  | &3Older to newer                                                                                                                              |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.order.publish_date.desc`         | String                  | &3Newer to older                                                                                                                              |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.claimall`                        | String                  | &6Claim All                                                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.asc`                             | String                  | &3Ascending                                                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.marketplace.desc`                            | String                  | &3Descending                                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.main.title`                                  | String                  | &9MarketPlace                                                                                                                                 |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.main.idsearch`                               | String                  | &eSearch By ID                                                                                                                                |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.main.namesearch`                             | String                  | &eSearch By Name                                                                                                                              |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.main.loresearch`                             | String                  | &eSearch By Lore                                                                                                                              |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.main.allsearch`                              | String                  | &eSearch all MarketPlace                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.main.categories`                             | String                  | &eSearch Categories                                                                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.categories.title`                            | String                  | &eSelect a category                                                                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.deliveries`                         | String                  | &5Deliveries ({amount})                                                                                                                       |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.gotosearch`                         | String                  | &7Go to Search Menu                                                                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.unclaimed`                          | String                  | &dWaiting for money claim                                                                                                                     |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.unbought`                           | String                  | &cUnbought listings                                                                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.cancelled`                          | String                  | &cCancelled/Expired listings                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.removed`                            | String                  | &aYou remove succesfully your listing &6{listing}!                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.deliveries.claimed`                          | String                  | &7You claimed a delivery!                                                                                                                     |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.deliveries.lore`                             | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.deliveries.title`                            | String                  | &6Your deliveries                                                                                                                             |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.history.purchases`                  | String                  | &3Purchases History                                                                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.history.purchasesLore`              | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.history.sales`                      | String                  | &9Sales History                                                                                                                               |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.history.salesLore`                  | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.claims.title`                       | String                  | &9Claim menu                                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.listings.claims.claimlore`                   | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.confirm.title`                               | String                  | &aConfirm Purchase                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.confirm.cancel`                              | String                  | &cCancel                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.confirm.seller`                              | String                  | &7Seller:&6 {seller}                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.confirm.price`                               | String                  | &7Price:&6 ${price}                                                                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.confirm.confirm.name`                        | String                  | &aPurchase                                                                                                                                    |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.confirm.confirm.lore`                        | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.idsearch.title`                              | String                  | &3Search By ID                                                                                                                                |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.idsearch.info`                               | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.my.title`                                    | String                  | &5My Listings                                                                                                                                 |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.background.item`                       | String                  | STAINED_GLASS_PANE                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.background.subid`                      | Integer                 | 7                                                                                                                                             |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.background.name`                       | String                  | &0                                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.changemenu.item`                       | String                  | ARROW                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.purchasesHistory.item`                 | String                  | ENCHANTED_BOOK                                                                                                                                |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.unbought.item`                         | String                  | NAME_TAG                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.deliveries.item`                       | String                  | MINECART                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.cancelled.item`                        | String                  | BARRIER                                                                                                                                       | This may vary in versions                                                                                                                           |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.salesHistory.item`                     | String                  | BOOK                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.claimNormal.item`                      | String                  | GOLDEN_APPLE                                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.claimNotification.item`                | String                  | GOLDEN_APPLE                                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.claimNotification.subid`               | Integer                 | 1                                                                                                                                             |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.searchName.item`                       | String                  | NAME_TAG                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.searchID.item`                         | String                  | APPLE                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.searchCategories.item`                 | String                  | BOOKSHELF                                                                                                                                     |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.searchLore.item`                       | String                  | BOOK                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.searchAll.item`                        | String                  | GOLDEN_APPLE                                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.back.item`                             | String                  | REDSTONE                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.confirmCancel.item`                    | String                  | REDSTONE_BLOCK                                                                                                                                |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.confirmPurchase.item`                  | String                  | WOOL                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.confirmPurchase.subid`                 | Integer                 | 5                                                                                                                                             |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.page.item`                             | String                  | FEATHER                                                                                                                                       |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.pageNext.item`                         | String                  | ARROW                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.pageBack.item`                         | String                  | ARROW                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.priceOrder.item`                       | String                  | ARROW                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.amountOrder.item`                      | String                  | COBBLESTONE                                                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.timeOrder.item`                        | String                  | WATCH                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`menu.items.claimAll.item`                         | String                  | GOLDEN_APPLE                                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`misc.disabled`                                    | String                  | &cThis feature is currently disabled!                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`misc.nomoney`                                     | String                  | &cYou don't have money to perform this action                                                                                                 |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`searches.categories`                              | Boolean (true or false) | false                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`searches.name`                                    | Boolean (true or false) | true                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`searches.id`                                      | Boolean (true or false) | true                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`searches.lore`                                    | Boolean (true or false) | true                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.tools.name`                            | String                  | &bTools                                                                                                                                       |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.tools.icon`                            | String                  | WOOD_PICKAXE                                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.tools.description`                     | String                  | &7Axes, Pickxes, Hoes and more tools!                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.tools.items`                           | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.equipment.name`                        | String                  | &5Equipment                                                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.equipment.icon`                        | String                  | IRON_HELMET                                                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.equipment.description`                 | String                  | &7Armors of any kind                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.equipment.items`                       | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.blocks.name`                           | String                  | &7Blocks                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.blocks.icon`                           | String                  | DIRT                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.blocks.description`                    | String                  | &bAll the blocks you can imagine                                                                                                              |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.blocks.items`                          | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.weapons.name`                          | String                  | &6Weapons                                                                                                                                     |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.weapons.icon`                          | String                  | STONE_SWORD                                                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.weapons.description`                   | String                  | &7Swords, bows and arrows                                                                                                                     |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.weapons.items`                         | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.redstone.name`                         | String                  | &cRedstone                                                                                                                                    |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.redstone.icon`                         | String                  | REDSTONE                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.redstone.description`                  | String                  | &7Everything you need to\n&7create redstone contraptions                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`categories.redstone.items`                        | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`chatsearch.lore`                                  | String                  | &aWrite in chat the lore you want to search (- to cancel):                                                                                    |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`chatsearch.name`                                  | String                  | &aWrite in chat the name you want to search (- to cancel):                                                                                    |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`chatsearch.cancel`                                | String                  | -                                                                                                                                             |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`chatsearch.cancelled`                             | String                  | &cSearch cancelled                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`chatsearch.timeout_seconds`                       | Integer                 | 60                                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`purchase.nomoney`                                 | String                  | &cYou don't have money to purchase this item!                                                                                                 |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`purchase.noavailable`                             | String                  | &cSorry, this item is no longer available                                                                                                     |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`purchase.purchase`                                | String                  | &aYou purchase &6{item}&a successfully                                                                                                        |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`purchase.notification`                            | String                  | &6{buyer}&a buy your &6{item}&a claim your money in &7/market my                                                                              |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`purchase.notificationJoin`                        | String                  | &aYou have &6{listings}&a listings to claim (Use &7/market my&a to claim it)!                                                                 |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`shout.permission`                                 | String                  | market.shout                                                                                                                                  |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`shout.message`                                    | String                  | &6{player}&3 published &6{item}&3 in the marketplace                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`shout.click`                                      | String                  | &7[Click here to open {player}'s shop]                                                                                                        |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`date.format`                                      | String                  | dd/MM/yy                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`date.now`                                         | String                  | just now                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`date.seconds`                                     | String                  | {time} seconds ago                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`date.minutes`                                     | String                  | {time} minutes ago                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`date.never`                                       | String                  | Never                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`money.format`                                     | String                  | #,###.00                                                                                                                                      |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`money.formatLocale`                               | String                  | en-US                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.sellerTax`                                    | Decimal/Double          | 1.35                                                                                                                                          | Tax percent to the seller when the money its claimed (0-100)                                                                                        |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.buyerTax`                                     | Integer                 | 0                                                                                                                                             | Extra tax that the buyer have to pay (percentage from the original price, 0-100)                                                                    |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.webPurchaseTax`                               | Decimal/Double          | 0.0                                                                                                                                           | The extra percentage of the total price payed on purchasing through web-client                                                                      |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.publish.permissions`                          | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.publish.default`                              | Decimal/Double          | 0.0                                                                                                                                           |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.publish.confirm`                              | String                  | &cBy publishing this item ${money} (A {tax}% of the raw price) will be withdrawn from your account, please type this command again to confirm |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.publish.confirm_cancel`                       | String                  | &cPublish confirm cancelled                                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.publish.confirm_time`                         | Integer                 | 5                                                                                                                                             | After this time (in seconds) the confirm option will be canceled                                                                                    |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.publish.nomoney`                              | String                  | &cSorry but you have not enough money to pay publish taxes (${money})                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.publish.return_on_cancel`                     | Boolean (true or false) | false                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.publish.return_on_cancel_expired`             | Boolean (true or false) | false                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`tax.publish.return_message`                       | String                  | &a${amount} has been deposited to your account                                                                                                |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`timeout.default`                                  | String                  | 7d                                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`timeout.permissions`                              | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`placeholderapi.latest`                            | String                  | &6{item} &c{price}$ &7({seller})                                                                                                              |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`langutils.default`                                | String                  | en_us                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`blacklist.enabled`                                | Boolean (true or false) | false                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`blacklist.message`                                | String                  | &cYou cannot publish this item in the market!                                                                                                 |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`blacklist.items`                                  | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`blacklist.lore_enabled`                           | Boolean (true or false) | false                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`blacklist.lores`                                  | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`blacklist.name_enabled`                           | Boolean (true or false) | false                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`blacklist.names`                                  | String list             | This is a list, click on the name to see it                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.enabled`                           | Boolean (true or false) | false                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.debug`                             | Boolean (true or false) | false                                                                                                                                         |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.url`                               | String                  |                                                                                                                                               |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.botName`                           | String                  | MarketPlace                                                                                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.botAvatar`                         | String                  | https://www.spigotmc.org/data/resource_icons/48/48526.jpg                                                                                     |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.notification.publish.enabled`      | Boolean (true or false) | true                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.notification.publish.title`        | String                  | New Item Published                                                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.notification.publish.description`  | String                  | **{player}** published **{item}** for **${price}**                                                                                            |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.notification.publish.color`        | String                  | #fec601                                                                                                                                       |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.notification.purchase.enabled`     | Boolean (true or false) | true                                                                                                                                          |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.notification.purchase.title`       | String                  | Item Purchased                                                                                                                                |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.notification.purchase.description` | String                  | **{buyer}** purchased **{item}** for **${price}** published by **{seller}**                                                                   |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :doc:`discordWebhook.notification.purchase.color`       | String                  | #30e539                                                                                                                                       |                                                                                                                                                     |
+---------------------------------------------------------+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
