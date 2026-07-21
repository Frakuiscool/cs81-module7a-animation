What part of the code was most confusing and why?

The cycleCount logic. It doesn't count every frame — it only goes up once per full loop through the 5 frames (index % frames.length === 0).
So maxCycles = 10 actually means 50 total frame changes (25 seconds), not 10. That wasn't obvious at first glance.

How does the animation help visualize asynchronous behavior?

setInterval runs its code every 500ms in the background, without freezing the rest of the page. 
The cycling emoji/dots make that "background ticking" visible — you can literally watch the delay happen instead of the page just pausing until it's done.

What did you change or improve, and what effect did it have?

I added a progress bar that fills up as cycleCount increases, plus a background color change when loading finishes.
It uses the same counters already in the code, and gives the user a clearer, more satisfying sense of progress than the spinner alone.
