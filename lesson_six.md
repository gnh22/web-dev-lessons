# Lesson 6: Making things more responsive

* I tried to reference some of my notes from a class I took last Fall semester, but asking chatGPT was just way faster and more effective, so here is what I asked it/got from it:
  * Me:
      > display:inline-grid; what does this do
  * Chat:
      
      > display: inline-grid; is a CSS property value that combines two concepts:
      >   * inline — The element behaves like an inline element in terms of layout. That means it flows with text and other inline elements and does not break onto a new line like a block element would.
      >   * grid — The element becomes a grid container, meaning you can use CSS Grid properties inside it to arrange its children in rows and columns.

  * Me:
      > i have a container with 2 sub containers, how do i put the items in the sub containers next to each other (on the same line)
  * Chat:
      > To put the items inside two sub-containers next to each other (on the same line), you'll want to make sure:
      >   * The parent container arranges the sub-containers side by side.
      >   * The sub-containers themselves arrange their own child items side by side.
  * Me:
      > align-items:center; why did this only center them vertically and not horizontally
  * Chat:
      > * justify-content: controls horizontal alignment (in a row)
      > * align-items: controls vertical alignment
  * Me:
      > how do i make text overlay an image in css
  * Chat:
      ```
      <div class="image-container">
        <img src="your-image.jpg" alt="Example">
        <div class="overlay-text">Your Text Here</div>
      </div>
      ```
      ```
      .image-container {
        position: relative;
        display: inline-block; /* keeps container tight to image */
      }
      
      .image-container img {
        display: block; /* removes whitespace below image */
        width: 100%; /* optional */
      }
      
      .overlay-text {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%); /* centers the text */
        color: white;
        font-size: 24px;
        font-weight: bold;
        text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.7); /* makes text readable */
      }
      ```
* and this is what my CSS looks like currently (in all it's messy glory):
    ```
    .container {
    margin-top:3%;
    display:flex;
    grid-auto-flow:columns;
    /* background-color: pink;  */
    /* align-items:center; vertically centered */
    justify-content:center; /* horizontally centered */
    }
    
    .container h1{
        /* background-color: orange; */
        height:200px;
        width:350px;
        /* position:absolute;
        left:850px;
        top:175px; */
        margin-top:7%;
        font-size: 72;
        color:#22577a;
        font-family: 'Arima Koshi', cursive;
        line-height: 1.1;    /*lessen white space between two lines of text*/
    } 
    
    .photo {
        /* background-color:orange; */
    }
    
    .info {
        margin-left:2%;
        /* background-color: grey; */
    }
    
    .profilephoto{
        width:550px;
        height:auto;
        /* position:absolute;
        left:275px;
        top:100px; */
    } 
    
    .stickynote-container {
        position:relative;
        display:inline-block;
        /* background-color:green; */
    }
    
    .stickynote-container img{
        display:block;
    }
    
    .stickynote-container p {
        font-size:26;
        font-style:italic;
        font-family:'Cairo', sans-serif;
        line-height:1.2;
        position:absolute;
        margin-left:5%;
        margin-right:5%;
        top:15%;
    }
    
     .notepic{
        /* position:absolute;
        left:850px;
        top:355px; */
        width:350px;
        height:auto;
    }
    ```



    
