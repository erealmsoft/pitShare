## wrong
var newObject = _.merge(user, {newKey: 'tester'})
`user` is an mongoose model object. `newObject` will be the same user object without merging newKey property.

## right way
var newObject = _.merge(user.toJSON(), {newKey: 'tester'})
