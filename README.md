# Server-APP-TodoIst
# Server APP TodoIst - Project 3 Repository II

**TODOIST - Read Me - Client**


# Description:
Improve your professional & Personal life satisfaction. Organize your to do tasks in an easy and clear way to simplify your daily routine.

## User Stories:

- **404** - user warning that the page doesn’t exist 

- **500** - user warning that something in the page isn’t working

- **homepage** -  Access the root to create the next To do list

- **hsign up** - Access all the available features of the website login - log in to personal account

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

Routes:

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
Homepage
CSS
HTML


# Models:

- ```To Do Model: 
 
const mongoose = require("mongoose");
const Todo = mongoose.Schema({
  text: {
    type: String,
  },
});
module.exports = mongoose.model("Todo", Todo);
```

- ``` User Model:
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

# Links:

Trello
Trello board

# Git:
Server Repository Link
Client Repository Link
