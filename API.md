RESTful API framework for how to set up and follow
**RE**presentational
**S**tate
**T**ransfer

HTTP request between client and server 

**the rules** to make API restful:
using HTTP request verbs (language): get, post, put, patch, delete
use specific pattern of Routes/Endpoint URLs

app.get / read to get the server to bring what is requested 
app.post / create to add and save to the database 
app.put / app.patch / update to update the data 
put -> replace in full
patch -> replace an element patch request to the server only updates the one element rather than the entire entry
app.delete / delete 

chaining method is commonly used to reduce length of code as below, the app waits for the request and then executes the block of code associated with the http verb
the below targets the "/articles" route and **all** of the articles as a result
```javascript
app.route("/articles")
.get(function(req,res){
    Article.find(function (err, foundArticles){
        if (!err) {
            res.send(foundArticles)
        } else {
        res.send(err);
    }})
})
.post(function(req,res){
    const newArticle = new Article({
        title: req.body.title,
        content: req.body.content
    });
    newArticle.save(function(err){
        if(!err) {
            res.send("successfully added a new article")
        } else {
            res.send(err);
        }
    });
})
.delete(function(req,res){
    Article.deleteMany( function(err){
        if (!err){
            res.send("successfully deleted all articles");
        } else {
            res.send(err);
        }
    })
});
```

below targets specific article in the articles collection 
```javascript
app.route("/articles/:articleName")
.get(function(req,res){
    Article.findOne({title: req.params.articleName}, function(err, foundArticle){
        if (!err){
            res.send(foundArticle);
        } else {
            res.send("no article found");
        }
    })
})
.put(function(req,res){
    Article.replaceOne({title: req.params.articleName},
        {title: req.body.title, content: req.body.content},
        function(err){
            if (!err) {
                res.send("successfully updated the acrticle")
        }})
})
.patch(function(req,res){
    Article.updateOne({title: req.params.articleName},
        {$set: req.body},
        function(err){
            if(!err){
                res.send("successfully updated the article")
            } else {
                res.send(err)
            }
        })
})

.delete(function(req,res){
    Article.deleteOne({title: req.params.articleName}, function(err){
        if(!err){
            res.send("successfully deleted the article")
        } else {
            res.send(err);
        }
    })
});
```

to work with non-existent API you can submit requests and responses via postman

also you use Studio 3T free for MongoDB for the front end of the database 

you can as well view database and data within terminal follow mongodb language?no sql
