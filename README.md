# practise-graphql-flask
Practise working with graphene and SQLAlchemy to create Graphql interface

1. Start a virtual environment
2. pip3 install flask flask-graphql flask-migrate flask-sqlalchemy graphene graphene-sqlalchemy
3. Import db in terminal and write some user/post data
4. python app.py runserver

When ran hello world reached at http://localhost:5000
While GraphQl interface reached at http://localhost:5000/graphql

Example query method:
{
  allPosts{
    edges{
      node{
        title
        body
        author{
          username
        }
      }
    }
  }
}

Example mutation method:
mutation {
  createPost(username:"username you have given while adding db data", title:"Hello 2", body:"Hello body 2"){
    post{
      title
      body
      author{
        username
      }
    }
  }
}
