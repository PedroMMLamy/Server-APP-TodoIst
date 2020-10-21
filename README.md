# Server-APP-TodoIst
# Server APP TodoIst - Project 3 Repository II

**TODOIST - Read Me - Client**


# Description:
Improve your professional & Personal life satisfaction. Organize your to do tasks in an easy and clear way to simplify your daily routine.

## User Stories:

- **404** - user warning that the page doesn’t exist 

- **500** - user warning that something in the page isn’t working

- **homepage** -  Access the root to create the next To do list

- **sign up** - Access all the available features of the website login - log in to personal account

- **logout** - log out from personal account to main page 

- **To do list** - All the created todo´s 

- **create To do** - create a new To do 

- **edit To do** - edit a created To do 

- **To do** - written details of a task

- **Delete To do** - delete a task

- **profile** - personal list of To do’s

- **other profiles** - other users personal list of To do’s


# Backlog:
Other features besides the mvp scope:
Task Category (Professional/Personal)

## Routes:

- <Route
            exact
            path='/'
            render={(props) => <Home {...props}  setUser={this.setUser} />}
            render={(props) => <Home {...props}  setUser={this.setUser} todos={this.state.todos} toggleTodoDone={this.toggleTodoDone} removeTodo={this.removeTodo} />}
          />

-   <Route
            path='/signup'
            render={(props) => <Signup {...props} setUser={this.setUser} />}
          />
 -  <Route
            path='/login'
            render={(props) => <Login {...props} setUser={this.setUser}/>}
          />
      
      
  -  <Route
            path='/todos'
            render={(props) => <Todos {...props} setUser={this.setUser}  newTodoChanged={this.newTodoChanged} formSubmitted={this.formSubmitted} toggleTodoDone={this.toggleTodoDone} removeTodo={this.removeTodo} allDone={this.allDone} todos={this.state.todos} newTodo={this.state.newTodo} />}
          />
      
  -   <Route
            path='/user'
            render={(props) => <CurrentUser {...props} setUser={this.setUser}/>}
          />
          
          
  -   <Route render={() => <h2> 404 </h2>} />
        </Switch>
        {/ <Todos 
          additem={this.addItem} 
          inputElement={this.inputElement}
        />}
      </div>
    );
  }
}
 

- <Route
            path='/'
            render={(props) => <Home {...props} setUser={this.setUser} />}
          />
          <Route
            path='/signup'
            render={(props) => <Signup {...props} setUser={this.setUser} />}
          />
          <Route
            path='/login'
            render={(props) => <Login {...props} setUser={this.setUser}/>}
          />*/
          

# Frontend:
- Homepage
- CSS
- HTML


# Models:

- To Do Model:

```  
 
const mongoose = require("mongoose");
const Todo = mongoose.Schema({
  text: {
    type: String,
  },
  user_id:String,
});
module.exports = mongoose.model("Todo", Todo);
```

- User Model:

``` 
const mongoose = require('mongoose');
const Schema = mongoose.Schema;

const userSchema = new Schema({
  username: String,
  password: String
}, {
    timestamps: {
      createdAt: 'created_at',
      updatedAt: 'updated_at'
    }
  });

const User = mongoose.model('User', userSchema);
module.exports = User;
```


## API Endpoints (backend routes)

| HTTP Method | URL                        | Request Body            | Success status | Error Status | Description                                                                                                                     |
| ----------- | -------------------------- | ----------------------- | -------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| GET         | `/auth/session `           | Saved session           | 200            | 404          | Check if user is logged in and return profile page                                                                              |
| POST        | `/auth/signup`             | {name, email, password} | 201            | 404          | Checks if fields not empty (422) and user not exists (409), then create user with encrypted password, and store user in session |
| POST        | `/auth/login`              | {username, password}    | 200            | 401          | Checks if fields not empty (422), if user exists (404), and if password matches (404), then stores user in session              |
| POST        | `/auth/logout`             | (empty)                 | 204            | 400          | Logs out the user                                                                                                               |
| GET         | `Provider/profile/list`    |                         |                | 400          | Show series elements                                                                                                            |
| GET         | `Provider/profile/:id`     |                         |                |              | Show specific element                                                                                                           |
| PUT         | `Provider/profile/:id`     |                         | 200            | 400          | Edit specific element                                                                                                           |
| DELETE      | `Provider/profile/:id`     |                         | 201            | 400          | delete element                                                                                                                  |
| GET         | `User/profile/list`        |                         |                | 400          | Show series elements                                                                                                            |
| GET         | `User/profile/:id`         |                         |                |              | Show specific element                                                                                                           |
| PUT         | `User/profile/:id`         |                         | 200            | 400          | Edit specific element                                                                                                           |
| DELETE      | `User/profile/:id`         |                         | 201            | 400          | delete element                                                                                                                  |
| POST        | `/requestedservice/create` |                         | 204            | 400          | Ask for service, and create requested service.                                                                                  |
| GET         | `/requestservice`          |                         | 204            | 400          | Show ask service page                                                                                                           |
| GET         | `/requestedservice/:id`    |                         | 204            | 400          | Show specific requestedservice                                                                                                  |
| GET         | `/requestedservice/list    |                         | 204            | 400          | Show series requestedservice                                                                                                    |
| POST        | `/acceptedservice/create`  |                         | 204            | 400          | Accept for service, and create requested service.                                                                               |
| GET         | `/acceptedservice/:id`     |                         | 204            | 400          | Show specific acceptedservice                                                                                                   |
| GET         | `/acceptedservice/list     |                         | 204            | 400          | Show series acceptedservice                                                                                                     |
| POST        | `/review/create`           |                         | 204            | 400          | create a review                                                                                                                 |
| GET         | `/review/:id`              |                         | 204            | 400          | Show specific review                                                                                                            |
| GET         | `/review/list`             |                         | 204            | 400          | Show series review                                                                                                              |
| DELETE      | `/review/:id`              |                         | 201            | 400          | delete review  

# Links:

Trello
Trello board

# Git:
Server Repository Link
Client Repository Link
