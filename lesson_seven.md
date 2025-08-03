# Span

I wanted to make my custome "button" image that has a text overlay a real button by giving it a hyper link, but when I went to do that, it through off all of my formatting! So, I 
turned to chat for some guidance on what to do next.

Me: can you do this:

  ```
  <a href="#learnmore">
          <img src="static/images/button.png" alt="blue button" class="blue-button">
          <p>learn more</p>
  </a>
  ```

Chat basically said you shouldn't use "p" in an href, but "span" instead.

So I did this:

```
  <a href="#learnmore" class="learn-more-link">
          <img src="static/images/button.png" alt="blue button" class="blue-button">
          <span>learn more</span>
  </a>
```

And my formatting was still all wonky so I asked chat about that as well:

Me: i want the text to overlay the button

And it gave me an idea of some changes to make, so here is my before and after:

Before:
  
  ```
  .bottom-area{
      /* background-color: orange; */
      display:flex;
      justify-content: center;
      align-items:center;
      margin-top:3.5%;
  }
  .bottom-area p{
      position:absolute;
      color:#353F4F;
      font-family: 'Arima Koshi', cursive;
      font-size:28px;
  }
  .blue-button{
      width:200px;
      height:auto;
      
  }
  ```

After:

  ```
  /* positions the button in the bottom center */
   .bottom-area{
      /* background-color: orange; */
      display:flex;
      justify-content: center;
      align-items:center;
      margin-top:3.5%;
  } 
  
  /*positions the text as centered within the button */
  .bottom-area span{
      position:absolute;
      top:20%;
      left:15%;
      color:#353F4F;
      font-family: 'Arima Koshi', cursive;
      font-size:28px;
  }
  
  .blue-button{
      width:200px;
      height:auto;
  }
  
  /* positions the text to be somewhere in the button */
  .learn-more-link{
      position:relative;
      display:inline-block;
      text-decoration:none;
  }
  
  .bottom-area:hover .blue-button {
      transform: scale(1.05);
      transition: transform 0.2s ease;
  }
  ```


