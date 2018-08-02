```js
describe ("lobby", ()=>{
	it ("should have a user info session")
	it ("should have a list of online friend (future dev)")
	it ("should have a button to join random public room")
	it ("should have a session for create private room")
	it ("should have a session for joining private room")
    it ("should check if user comes through an invitation link")

	describe ("user info session", ()=>{
	it ("should show player icon, username, scores, rank")
	it ("should pop up a moddle with more info when clicked on")
    })

    describe ("friend list", ()=>{
        it ("should show all friends from social login account")
        describe ("each friend tag", ()=>{
            it ("should open friend info when clicked on")
        })
    })

    describe ("join random public room button", ()=>{
        it ("should allow player join first public room with an empty slot")
        it ("should redirect player to game page")
    })

    describe ("create private room session", ()=>{
        it ("should have input box / drop down menu for game settings)
        it ("should allow settings on difficulty")
        it ("should allow settings on category")
        it ("should allow settings on number of rounds")
        it ("should have a create game button")
        it ("should have a delete room button")
        it ("should have a start game button")
        it ("should show which player is in the created room")
        it ("should show which player is in the room and is ready to start game")

        descrbe ("create game button", ()=>{
            it ("should only be available to creator")

            describe ("when create game button is clicked", ()=>{
                it ("should create a new room in DB and socket with chosen settings")
                it ("should change to 'Delete Room' button")
                it ("should activate 'Ready' button")
                it ("should show the creator is in the created room")
            })
            describe ("when delete room button is clicked", ()=>{
                it ("should kick ALL players out of the game room, ie change active_game_id")
                it ("should change 'Delete Room' button back to 'Create Game'")
                it ("should in-activate 'Ready' button")
                it ("should restore all setting inputs to default")
            })
        })

        describe ("ready button", ()=>{
            describe ("when 'Ready' button is clicked", ()=>{
                it ("should show everyone in this room that this player is in the room and is ready to start game")
                it ("should change to 'Not ready' button, ie toggle CSS to show state")
            })

            describe ("when 'Click if not ready' button is clicked", ()=>{
                it ("should show everyone in this room that this player is in the room")
                it ("should change to 'Ready' button, ie toggle CSS to show state")
            })
        })

        describe ("start game button", ()=>{
            it ("should only be available to creator")
            it ("should only activate when all player in room is ready")

            describe ("when start game button is clicked", ()=>{
                it ("should redirect all player in room to game page")
            })
        })

        describe ("invitation link", ()=>{
            it ("should be generated when a room is created")
            it ("should come with a copy link button")
            it ("should have a structure of ......")
        })
    })

    describe ("join private room session", ()=>{
        it ("should have a link input box")
        it ("should have a join button")

        describe ("link input box", ()=>{
            it ("should allow player to paste invitation link")
        })
        describe ("join button", ()=>{
            it ("should only activate when a link is entered")
            it ("should allow player to join the room when clicked")
            it ("should prompt player room does not exist if room is not found")
        })
        describe ("when a player join a room successfully", ()=>{
            it ("should in-activate both input box and join button")
            
            describe ("create private room session", ()=>{
                it ("should be populated with game room details")
                it ("should only activate 'Ready' button")
            })

            describe ("when creator starts game", ()=>{
                it ("should redirect player to game page")
            })
        })
    })

    describe ("invitation link", ()=>{
        it ("should be generated when a game room is created")
        it ("should be unique")
        it ("should consist of `game_id` param")
    })

    describe ("if user comes through an invitation link", ()=>{
        it ("should automatically join room as if user manually joined it")
        // read "join private room session" for details"
    })
})

```