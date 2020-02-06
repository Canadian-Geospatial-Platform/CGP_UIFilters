# CGP_UIFilters 
this the UI filters repository.

# built with 
- Bootstrap 4.3
- JQuery 3.4.1
- Node Js 
 
# this is prototype according with requirements for Filtering and search.

![Image](https://github.com/Canadian-Geospatial-Platform/CGP_UIFilters/blob/master/docs/proto/1.png)

![Image](https://github.com/Canadian-Geospatial-Platform/CGP_UIFilters/blob/master/docs/proto/2.png)


# Data Result
for each checkbox selected will build dynamically a JSON Structure following:

[{ id: "1", title: "DataSet" }, { id: "2", title: "WebServices" }]


using Jquery Ajax will pass calling the AWS API 
```
$.ajax(
      {
      url:'https://url-apiv1',
      headers:{'Content-type':'application/json',
              'Access-Control-Allow-Origin':'*'
              },
      CrossDomain:true,
      Type:'POST',
      dataType:'application/jSon',
      data:JsonString,
      Success:function(data){
        console.log(data);
      },
      error: function(data){
        console.log("error = "+JSON.stringify(data));
      }
    })//end $.ajax
