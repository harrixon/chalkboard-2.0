```js
describe ("game page", ()=>{
	it ("should have 2 canvas")
	it ("should have a chat box with input")
	it ("should have a timer")
	it ("should display the keyword for drawer")
	it ("should display '_' to replace each letter in keyword for guesser")
	it ("should display active player")
	it ("should display game info")
	it ("should be mobile responsive")
	it ("should always be in landscape mode")
	it ("should log every player event")

	describe ("disconnect event", ()=>{
		describe ("on player disconnects", ()=>{
			it ("should goes on until game ends")
		})
		describe ("while a player is disconnected", ()=>{
			it ("should allow disconnected player to reconnect")
			it ("should not wait for disconnected player to reconnect to proceed")
			it ("should update game table's 'active_player_id')
		})
		describe ("on player reconnects", ()=>{
			it ("should populate updated game / player info")
			it ("should always re-populate canvas for reconnected player")
			it ("should update game table's 'active_player_id')
		})
		describe ("when only one player is left in room", ()=>{
			it ("should wait for disconnected player for certain time (eg. 30s)")
			it ("should kick the only player out and destory room")
			it ("should update game table's 'active_player_id'")
			it ("should update user table's 'active_game_id'")
			it ("should redirect the player back to lobby")
		})
		describe ("when a room is destoryed", ()=>{
			it ("should clear event log in REDIS")
		})
		describe ("when a disconnected player reconnects but room no longer exist", ()=>{
			it ("should update user table "active_game_id")
			it ("should redirect player back to lobby")
		})
	})

	describe ("game logic", ()=>{
		describe ("canvas one", ()=>{
			it ("should allow drawing")
		})
		describe ("canvas two", ()=>{
			it ("should block access to canvas 1 for guesser , with z-index +3000)
			it ("should allow access to canvas for drawer , with z-index -1)
			it ("should block access to canvas 1 during round change
		})
		describe ("drawing tools", ()=>{
			it ("should be visible to drawer only")
			it ("should provide color change tool")
			it ("should provide brush/pen tool")
			it ("should provide eraser tool")
		})
		describe ("chat box", ()=>{
			describe ("chat history", ()=>{
				it ("should always be available to all players")
				it ("should show all wrong input")
				it ("should replace correct answer with sys.msg.(eg. congrat xxx) ")
			})
			describe ("input box", ()=>{
				it ("should always block access to drawer")
				it ("should block access to guesser during round change")
				it ("should treat any input as a guess")
				it ("should be case-insensitive")
			}) 
		})
		describe ("timer", ()=>{
			it ("should start at chosen time limit, default 1min)
			it ("should (re-)start when round start, ie everyone ready")
			it ("should stop when time is up , or everyone guess correctly")
		})
		describe ("keyword", ()=>{
			it ("should be displayed to drawer")
			it ("should be displayed to guesser, but replace every letter with  '_' instead")
			it ("should be shown to all player during round change")
		})
		describe ("game info", ()=>{
			it ("should display all game settings")
			it ("should display which round currently at")
		})
		describe ("player info", ()=>{
			it ("should show all player in game")
			it ("should be arranged accoring to in-game score in descending order")
			it ("should display certain info of each player (info to show TBD) ")
		})
	})
})

```
