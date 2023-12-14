# The Selfie Sample Story

This repository reveals how [DreCapone's](https://open.spotify.com/artist/4Q4IYJ5TxabcXkd6U2NEcK?si=pwxHAzUrSQaGhRG3koMjEQ) Selfie Sample song came to be. If you haven't already, you can listen to it at: [Selfie Sample on Spotify](https://open.spotify.com/track/1PwnldgLzUDFLz0K9ZRZbn?si=5309c2311a3d420f).


## Sponsors and Creators
This is a project sponsored by [MathWorks](https://www.mathworks.com/) that showcases both their [MATLAB](https://www.mathworks.com/products/matlab.html) software and the amazing people who use it for creative purposes.

Three people played around with the ideas that culminated in the Selfie Sample song:

[DreVonne Hilton](https://www.linkedin.com/in/drevonne-hilton-403672199), the artist performing the Selfie Sample song, is a class of 2024 student at the [Olin College of Engineering](https://www.olin.edu/). He stays active in the Hip-Hop community while completing his undergraduate engineering degree in Electrical and Computer Engineering.

[Wynter Duncanson](https://www.linkedin.com/in/wynterjd) is a MathWorks employee and avid advocate for accessible STEM Education. She coached some of the ideation and coding aspects of the project.

[Amon Millner](https://www.linkedin.com/in/amon-millner-2653006b/) is an Associate Professor of Computing and Innovation at the Olin College of Engineering. He co-shaped the vision, assisted with the coding, and documented the process.


## Brainstorming the Idea

In January 2023, Amon invited Dre tell a story about a part of his journey to undergraduate engineering studies that he felt would be engaging to a public event for a multi-generational audience. Dre was excited to format his story as a rap, because he regularly expresses himself through rhyme. During a session when he was trying out different lyrics for his story/song, he imagined a scenario where the words he was writing could shape the beat he would ultimately rap over.

Dre explored multiple ways to link his vocals to his beat. Maybe the total number of vowels in his song lyrics could influence the amount of bass in the beat? Perhaps the number of three letter words in the lyrics could dictate the tempo of the beat? Ultimately, for the public event performance, Dre and Amon thought it would be fun for Dre to deliver his lyrics with Amon beatboxing a beat for him.


## Pivoting from Lyrics to Images

In September of 2023, Dre and Amon visited Wynter at the MathWorks campus. We revisited Dre's idea from January 2023 of having the words he spoke shape the beat he'd rap them over. in order to explore ways for MATLAB to contribute to a custom beat for Dre to pair with the next track he wrote for a special Spotify release.

We struggled to settle on a strategy to turn the lyrics into an input for a MATLAB program that would make sounds that could become core building blocks of a flow-worthy beat. Early in our meeting, we played with a [MATLAB project that acted as a virtual theramin](https://www.mathworks.com/academia/courseware/bytes-and-beats.html) - something that played constant sounds based on a mouse pointer's movement across an colored square image on the screen.

We noticed that the virtual theramin code caused the background color to change at the same time the sound changed based on every mouse move. We wondered whether we could riff off of that interaction: move a mouse across an image and make sounds that correspond to the color of the pixel. We pivoted to that idea and opened the theramin code to begin remixing it.


## Deciding Interaction Techniques

Before looking for the places in the theramin project code that we'd modify to change the program's functionality, we had to think about exactly what we wanted the new code to do. We decided that we wanted to start simple by having only four distinct sounds to result from users moving a mouse pointer across an image. We also shrunk the scope of our project down by focusing only on the grayscale range of colors between black and white.

We decided that darker gray/black pixels would be represented by numbers closer to 1. Lighter pixels approaching white would be represented as numbers closer to 255. To make 5 distinct sounds to be the basis of a Dre-made beat, we assigned a the first unique sound to mouse clicks that landed on pixels with a color value between approximately 43 and 85, a different sound to pixels with a color value between 86 and 127, yet another sound to pixels yielding color values between 128 and 169, and one other sound for pixels holding grayscale color values between 170 and 213. Any click on a pixel with a value lower than 43 or higher than 213 played the last sound.

The values we have in the code on this repo are numbers that would probably need to be adjusted if you try this out with a different image than what Dre used. You will also need to point the ImageSource line to your own photo file.




## Choosing an Initial Image

The album art of the Selfie Sample song is ![an image of him in a white shirt in front of green bushes](dre-selfie-sample-photo.png). Dre liked the image because it had colors that ranged from brown to white to green. He enjoys writing songs that are personal to him so this image features a logo of his hometown high school. We encourage those who play with this project using their own images to pick clothes, a background, or colors that are meaningful to you.


## Blending Starter Code with Class Code

To tackle the first task of converting a full color image into a grayscale one, Dre remembered that he had done that exact task in one of his first year classes at Olin. He quickly revisited the code from one of his old assignment submissions and found what he was looking for. He cut and pasted the code snippet and made the necessary modifications to incorporate it into the theramin code we were starting from.


## Enhancing the Beat

Once the selfie was sampled - moving a mouse around it and clicking the areas Dre wanted to produce a few sounds, Dre used his skills with [Bandlab](https://www.bandlab.com/) to add layers to the beat. Once he reached a point where he had two candidate beats, he wrote [lyrics](selfie-sample-lyrics.rtf) for each one and recorded 2 distinct draft versions: [V1](ss-draft-V1.mfa) and [V2](ss-draft-V2.m4a).

Dre had an idea of which version he wanted to release, but before he uploaded his favorite, he shared both song drafts with friends and colleagues. Dre considered the feedback he got from friends and NSBE Jr students. He had enough data to know that he wasn't the only one who preferred the second of his drafts, so he uploaded the Selfie Sample track to Spotify. He let people know that he dropped a new track through an Instagram post and got positive reactions.


## Capturing the Process

We put some of the photos we took along this journey into a Google Photos album. Check them out at: [Selfie Sample Behind the Scenes](https://photos.google.com/share/AF1QipMh_c0k2mr3T4ubkv0zlAKXFEW5Q2e3fuootz6CnOFQs-kM-SuPv-YshNeGeBeXoA?key=UlVzQjNZN2hqcmVYY2RrbWRKRFlraUM2YkFhMklB)


## Enabling More Selfie Samples

Anyone visiting this page can explore the code and media in this repository. You can download it and come up with your own variations. That may involve downloading the .mlx file onto your computer. If you have or get a [Github](https://github.com/) account, you can fork and clone the whole repository to keep track of the new revisions you try.

So far, the Selfie Sample crew has shown the process discussed here to multiple National Society of Black Engineers (NSBE) Junior Chapters in the Northeast Region. We have the materials on line to make it easier for people to try things like Selfie Sample out.


## Planning What's Next

We plan to make a Youtube video that shows "The Making of Selfie Sample." After showing what went into the process in the video, we hope to end it by challenging viewers to respond to the video by posting their remix ideas and creations.


## Requirements

This code runs in [MATLAB](https://matlab.mathworks.com/) - either the Desktop Version or the online version.
You will need a MATLAB account.
You can use any beat making software that you would like to enhance your beats.
Github accounts are optional.
