# Lesson 4: Adding Images

* used Google AI overview "how to alter image size in css" for:
  ```
  .about-me img{
    width:300px;
    height:auto;
  }
  ```
  to adjust the width and have the height auto adjust so it wouldn't get messed up
* used https://www.w3schools.com/css/css3_images.asp to make it round:
  ```
  .about-me img{
    width:300px;
    height:auto;
    border-radius:50%
  }
  ```
* used https://www.reddit.com/r/HTML/comments/hejvc3/how_do_i_position_my_image_in_different_places/  for positioning (may look into doing a flexbox?):
  ```
  .about-me img{
    width:550px;
    height:auto;
    border-radius: 50%;
    position:absolute;
    left:250px;
    top:150px;
  }
  ```
* used https://www.w3schools.com/howto/tryit.asp?filename=tryhow_css_zoom_hover for zooming in on the image when you hover:
  ```
  .about-me img{
    width:550px;
    height:auto;
    border-radius: 50%;
    position:absolute;
    left:250px;
    top:150px;
    transition:transform .5s;
  }

  .about-me img:hover{
    -ms-transform: scale(1.25); /* IE 9 */
    -webkit-transform: scale(1.25); /* Safari 3-8 */
    transform: scale(1.25); 
  }
  ```
  (not obsessed with this I think it could be better)
 
