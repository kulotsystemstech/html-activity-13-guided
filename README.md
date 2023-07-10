## HTML | Activity #13 (Guided): Video
In this activity, we will create a **Song Review Page** with the following content:

![final-output](assets/html-13--01-final-output.jpg)


### Development Setup
Create your `index.html` file inside the [**src**](/src) folder in this project,
then follow along with this guide.

To test your output, simply open it in your preferred web browser.


### Template
First, we need a regular HTML template that already contains relevant texts and layout.

![template](assets/html-13--02-template.jpg)

We will leave [comments](https://www.w3schools.com/html/html_comments.asp) for the parts that we will do later.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Song Misinterpretation on TikTok</title>
</head>
<body>
    <div class="header" align="center">
        <h1>Song Misinterpretation on TikTok</h1>
    </div>

    <div class="intro">
        <table width="100%" cellpadding="4">
            <tr>
                <td width="50%" valign="top">
                    <h2>"If We Ever Broke Up" Taken Out of Context</h2>
                    <p>
                        <b>"If We Ever Broke Up"</b> by <b>Mae Stephens</b>
                        is a captivating song that delves into the complexities
                        of a troubled romantic relationship.
                        The chorus, which includes lines like
                        <b><i>
                            "If we ever broke up, I'd never be sad"
                        </i></b>
                        and
                        <b><i>
                            "I'd call your dad and tell him all the shittiest
                            of things you said, if we ever broke up,"
                        </i></b>
                        seems to have caused some confusion for listeners.
                        Despite the lyrics suggesting negative dynamics,
                        some couples on <b>TikTok</b> have created cute videos
                        that seem to misunderstand the song's true meaning.
                    </p>
                    <p>
                        The song's beat, in terms of value,
                        sounds like Mae Stephens is expressing satisfaction
                        even in the face of a toxic relationship.
                        However, further analysis revealed that the song was more complex
                        than it was originally.
                        Her lyrics convey mixed emotions,
                        including frustration and a desire to fight back.
                        It's important to note that these quotes
                        do not necessarily reflect the dynamics
                        of a healthy or positive relationship.
                    </p>
                </td>
                <td width="50%">
                    <figure>

                        <!-- Official Music Video -->

                        <figcaption>
                            <b>Official Music Video:</b>
                            "If We Ever Broke Up" by Mae Stephens
                        </figcaption>
                    </figure>
                </td>
            </tr>
        </table>
    </div>

    <div class="tiktok">
        <div align="center">

            <!-- TikTok Video 1 -->
            

            <!-- (spacer) -->
            &nbsp;&nbsp;

            
            
            <!-- TikTok Video 2 -->
            

            
            <!-- (spacer) -->
            &nbsp;&nbsp;
            
            
            <!-- TikTok Video 3 -->

        </div>
    </div>

    <div class="conclusion">
        <table>
            <tr>
                <td>
                    <p>
                        While videos on TikTok featuring couples performing
                        "If We Ever Broke Up" as a happy hymn are certainly adorable,
                        it's important to realize the true meaning behind the song.
                        In doing so, we can more deeply appreciate the artist's intentions
                        and use music as a catalyst
                        for personal growth and reflection in our own relationships.
                    </p>
                </td>
            </tr>
        </table>
    </div>
</body>
</html>
```


### Defining Video Elements
To define a video element in HTML, we use the `<video>` tag.
Inside it, we nest one or more self-closing `<source/>` tags - each has
`src` attribute that contains the URL or path of the video file with a specified `type`.

Example:
```html
<video controls>
    <source src="video.mp4" type="video/mp4"/>
    <source src="video.ogg" type="video/ogg"/>
</video>
```

<p>
    <small>
        <b>NOTE:</b>
        We use multiple sources with different video file formats
        to provide options in the event that one format is not supported or available.
    </small>
</p>

The `controls` attribute in the video element is needed
to display the default video controls, such as *play*, *pause*, *volume*, and *full-screen toggle*.
The video may not show up in the browser if this attribute is missing.

#### Official Music Video
![official-music-video](assets/html-13--03-official-music-video.jpg)

For the **Official Music Video**, there's only one video source: `mp4`
```html
                        ...
                        
                        <!-- Official Music Video -->
                        <video controls width="100%">
                            <source
                                src="video/if-we-ever-broke-up--official-music-video.mp4"
                                type="video/mp4"
                            />
                        </video>
                        
                        ...
```

#### TikTok Video 1
![tiktok-video-1](assets/html-13--04-tiktok-video-1.jpg)

For **TikTok Video 1**, there are three video sources: `mp4`, `ogv`, and `webm`.

```html
            ...
            
            <!-- TikTok Video 1 -->
            <video controls loop width="200">
                <source src="video/if-we-ever-broke-up-krazyrai.mp4"  type="video/mp4" />
                <source src="video/if-we-ever-broke-up-krazyrai.ogv"  type="video/ogg" />
                <source src="video/if-we-ever-broke-up-krazyrai.webm" type="video/webm" />
            </video>
            
            ...
```

The `<video>` tag has other attributes such as:

| Attribute  | Description                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| `autoplay` | Start playing as soon as the video it is ready.                                                             |
| `loop`     | Start over again, every time the video is finished.                                                         |
| `poster`   | URL or path of an image to be shown while the video is downloading, or until the user hits the play button. |
| `width`    | Width of the video player.                                                                                  |
| `height`   | Height of the video player.                                                                                 |


***TODO:***
Complete all three TikTok Videos.

![todo](assets/html-13--05-todo.jpg)

You can find all the video files inside the [**video**](src/video) folder.
