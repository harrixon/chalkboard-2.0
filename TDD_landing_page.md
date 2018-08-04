```js
describe ("landing page", ()=>{
    it ("should allow social login")
    it ("should allow local login")
    it ("should have a very simple description of the web/game")

    describe ("social login", ()=>{
        it ("should let user login with one click")

        describe ("successful login", ()=>{
            it ("should redirect user to lobby page")
        })
        describe ("in-successful login, ()=>{
            it ("should prompt user to try again / error status")
        })
    })

    describe ("local login", ()=>{
        it ("should pop out a moddle when chosen")

        describe("local login moddle", ()=>{
            it ("should have a welcome / error msg")
            it ("should have a sign in button")
            it ("should have a sign up button")
            it ("should have a username input box")
            it ("should have a password input box")
            it ("should close when user click outside of moddle")

            describe ("username && password", ()=>{
                it ("should not be empty")
                it ("should only allow unique username")
                it ("should trigger err msg when empty && sign in/up button is clicked")
            })
            describe ("sign in", ()=>{
                it ("should allow user to login with username and pw provided")

                describe ("successful login", ()=>{
                    it ("should store user token in memory")
                    it ("should store session token")
                    it ("should redirect user to lobby page")    
                })
            })
            describe ("sign up", ()=>{
                it ("should allow user to sign up with username and pw provided")

                describe ("successful sign up", ()=>{
                    it ("should auto login for user, done by front end")
                })
            })
        })
    })

    describe ("redirect behavior", ()=>{
        it ("should redirect all 404 to landing page")
        it ("should redirect all un-authorized visit to landing page")

        describe ("access through invitation link", ()=>{
            describe ("if user is logged in", ()=>{
                it ("should redirect to lobby page with param")
            })
            describe ("if user is not logged in", ()=>{
                it ("should redirect to landing page")
            })
        })
        // Q: how do we process the invitation link param / game_id ?
    })

})

```