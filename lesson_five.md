# Lesson 5: Lots of stuff

Wednesday July 30th, 2025

I used PowerPoint (lol it works for me) to make a mockup of what I ideally would like my website to look like, 
and then I've spent most of the evening trying to make it happen!

1. New Background:
   * I wanted my background to resemble grid paper, so I asked chatGPT to help me generate it because the tool exists and I had no idea where to begin!
      ```
      body {
      font-family:'Times New Roman', Times, serif;
      background-color: #fff;
      /*chatGPT helped me generate this:*/
      background-image: 
          repeating-linear-gradient(
          to right, 
          rgb(134, 197, 246) 0, 
          rgb(134, 197, 246) 1px, 
          transparent 1px, 
          transparent 25px
          ),
          repeating-linear-gradient(
          to bottom, 
          #ccc 0,         /* it looks kinda good with these as cream and not also blue...*/
          #ccc 1px, 
          transparent 1px, 
          transparent 25px
          );
      }
      ```
   and unfortunately i don't think i could tell you **exactly** how this is working, but it's just the background soo i think a little mystery is fine.
2. Updated navigation bar
     * I did not like how the old one looked. The icon was throwing me off so I just got rid of it. New one feels much simpler and cleaner. The li part is still from an earlier
     * tutorial, only part I probably changed was centering it:
       ```
       .navbar {
        display:flex;
        /* background-color: rgba(146, 248, 91, 0.5); */
        margin:15px auto;
        justify-content: center;    /*puts items in navbar centered*/
        align-items:center;
        width:700px;
        }
       ```
3. Profile photo and sticky note decorations and stickers:
   * i had no idea how to recreate the cute sketch affect for the shapes that i made in powerpoint, BUT powerpoint has a cool feature where you can save
     the things you make as pngs, so i did that and imported the entire thing as an image and they look good!
4. Definitely some other things I am feeling too lazy to go through.

IMPORTANT: What to work on next time

Sooo... currently... all of my images and some text elements are ... position:absolute ... and I KNOW this is really not ideal. Anytime the screen changes
size these aren't responsive to it, so i know i need to figure out a grid layout since this involes some row AND column stuff, but i cannot a good tutorial on it. ugh. that is for another day. in the meantime i am happy with it!
