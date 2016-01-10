use promises and Deferred
Jquery ajax requests
```
function example(){
  var deferred = $.Deferred();
   $.getJSON(yqlAPI, function(){
      console.log("sucess");
  })
    .success(function(r){
         deferred.resolve(data);
    }
return deferred.promise();
}
function updates () {
    var promises=[];
  for (var i = 0; i < names.length; i++) {
    promises.push(example(names[i]));
  };
  $.when.apply($, promises).then(function() {
           var temp=arguments; // The array of resolved objects as a pseudo-array
    console.log(temp);           
  })
}```
