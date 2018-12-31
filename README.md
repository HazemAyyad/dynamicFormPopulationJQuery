# dynamicFormPopulationJQuery
Dynamic form population using JQUERY
# Sample for populating input field with Delete Button


<html>
<head>
    
    
<title>Add input field using jquery</title>


<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">


<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.6.3/css/all.css" integrity="sha384-UHRtZLI+pbxtHCWp1t77Bi1L4ZtiqrqD80Kn4Z8NTSRyMA2Fd33n5dQ8lWUE00s/" crossorigin="anonymous">


<script src="https://code.jquery.com/jquery-3.3.1.js" integrity="sha256-2Kok7MbOyxpgUVvAk/HJ2jigOSYS2auK4Pfzbm7uH60="  crossorigin="anonymous"></script>


<script>
$(document).ready(function() {
    var wrapper         = $(".myFields"); 
    $(add_button).click(function(e){ 
        e.preventDefault();
            $(wrapper).append('<div class="form-group"><label class="col-md-2" for="person">Person Name</label><input type="text" name="mytext[]" class="col-md-6"/><a href="#"	class="btn btn-danger btn-sm delFld"><span class="fas fa-trash-alt"></span>Delete</a></div>'); //add input box
    });
    
    $(wrapper).on("click",".delFld", function(e){ 
        e.preventDefault(); $(this).parent('div').remove();
    })
});
</script>


<style>
.container{padding:15px 10px;margin:15px 15px 15px 10px;}
.addNew{margin:0px 0px 0px 15px;}
</style>


</head>


<body>
    
    
<div class="container">
<div class="myFields"></div>
 <button id="add_button" class="addNew btn btn-success btn-sm"><span class="fa fa-plus"></span>Add New</button>
</div>


</body>


</html>
