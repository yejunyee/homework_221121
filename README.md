# index.html
<html>
    <script defer src="rfile.js"></script>
    <input type='file' accept='image/*' onchange='openFile(event)'><br>
    <img id='imageUpload'>
<html>
  
# rfile.js
  
  var openFile = function(file) {
  var input = file.target;
  var reader = new FileReader();
  reader.onload = function(){
    var dataURL = reader.result;
    var imageUpload = document.getElementById('imageUpload');
    imageUpload.src = dataURL;
  };
  reader.readAsDataURL(input.files[0]);
};
