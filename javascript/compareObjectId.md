## case 
```
var blogs; // array of Blog (mongoDB model)

var blogId = req.query.blogId;

blogs.forEach(function(blog){
  if (blog._id === blogId) {
    // do sth.
  }
});

```
But blog._id will never equal to blogId

## Solution

A straight == (or ===) comparison will compare the two objects by reference, not value. So that will only evaluate to true if they both reference the very same instance.

use `equals` instead of `===`

```
 if (blog._id.equals(blogId)) {
   // do sth.
 }
```

## references

[Mongoose: ObjectId Comparisons fail inconsistently](http://stackoverflow.com/questions/11060213/mongoose-objectid-comparisons-fail-inconsistently)
