```js
describe ("lobby", ()=>{
	it ("should have a user info session")
	it ("should have a list of online friend (future dev)")
	it ("should have a button to join random public room")
	it ("should have a session for create private room")
	it ("should have a session for joining private room")

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
        it ("should have a cancel button")
        it ("should show which player is in the created room")
        it ("should show which player is in the created room and ready to start game")

        describe ("create game button is clicked", ()=>{
            it ("should create a new room in DB and socket")
            it ("should change to 'Click when ready' button")
        })
    })
})

```