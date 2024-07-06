To build acustom form controls
html code:

!DOCTYPE html> 

<html> 

<head> 

    <title>Building custom control</title> 

    <link rel="stylesheet"

          type="text/css"

          href="style.css"> 

     <script src= 

"https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"> 

   </script> 

      

</head> 

<body> 

    <h2 style="color:green">custom controls</h2> 

    <strong>Custom form controls</strong> 

    <br/><br/> 

     <div class="select-container"> 

      <div class="option-container"> 

        <div class="option">Lemon</div> 

        <div class="option">Cherry</div> 

        <div class="option">Apple</div> 

        <div class="option">Strawberry</div> 

        <div class="option">Banana</div> 

        <div class="option">Pineapple</div> 

        <div class="option">Mango</div> 

        <div class="option">Papaya</div> 

        <div class="option">Orange</div> 

        <div class="option">Grapes</div> 

      </div> 

      <div class="selected">Select</div> 

    </div> 

    <script> 

       $( document ).ready(function() { 

           const selected = document.querySelector(".selected"); 

           const optionContainer =  

               document.querySelector(".option-container"); 

  

           const optionList = document.querySelectorAll(".option"); 

  

            selected.addEventListener("click", () => { 

              optionContainer.classList.toggle("active"); 

            }); 

  

            optionList.forEach((item) => { 

              item.addEventListener("click", () => { 

                selected.innerHTML = item.innerHTML; 

                optionContainer.classList.remove("active"); 

              }); 

            }); 

       }); 

    </script> 

</body> 

</html> 
