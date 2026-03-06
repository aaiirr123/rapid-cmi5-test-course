# Media Components Guide

Media elements allow you to include **audio, video, images, downloadable assets, and code snippets** inside your content.

These components make lessons more engaging and help present information in multiple formats.

***

# Audio

Audio files allow you to embed **voice narration, explanations, or recorded instructions** directly into the page.

**Common Uses**

* Instructor narration
* Podcast-style explanations
* Pronunciation guides
* Recorded feedback

**Notes**

* Supported formats typically include `.mp3`, `.m4a`, and `.wav`
* The `controls` attribute allows the user to play/pause and control volume
* Always provide a descriptive `title`

### Example

<audio src="./Assets/Audio/Recording (4).m4a" controls="true" data-audio-id="16548096-e22b-461c-9525-6a7f20053525" title="Recording (4)"></audio>

***

# Video

Videos allow you to embed **screen recordings, demonstrations, or instructional content**.

**Common Uses**

* Software walkthroughs
* Demonstrations
* Lectures
* Tutorials

**Notes**

* Large videos should be compressed to improve loading performance
* Provide clear titles
* Consider keeping videos under **5–10 minutes** for better engagement

### Example

<video src="./Assets/Videos/Screen Recording 2026-03-04 183338.mp4" controls="true" data-video-id="8884ae90-499c-4a77-9ba3-1bddc44fce74" title="Screen Recording 2026-03-04 183338"></video>

***

# Images

Images are useful for **diagrams, screenshots, illustrations, and branding**.

**Best Practices**

* Use descriptive `alt` text for accessibility
* Optimize images for web (PNG or WebP recommended)
* Avoid extremely large images

### Example

<img alt="RangeOS_Logo (1)" id="20260304183445-1fc5dc56-90ec-4a92-a70c-d24a9e5b6242" src="./Assets/Images/RangeOS_Logo (1).png" />

:::imageText{imageId="20260304183445-1fc5dc56-90ec-4a92-a70c-d24a9e5b6242" x="139.0625" y="70.4375"}
<span style="color: #ffffff;">  </span>**You Can Also Label an Image!**<span style="color: #ffffff;">  </span>
:::

***

# Downloadable Files

Download components allow users to **retrieve assets directly from the lesson**.

These are useful for:

* Lab materials
* Configuration files
* Source code
* Reference documents

**Notes**

* Files are defined using JSON metadata
* Each file requires:
  * `name`
  * `path`
  * `type`
* Multiple files can be included in the same download block

### Example

:::download
```json
{
 "files": [
  {
   "name": "RangeOS_Logo (1).png",
   "path": "RangeOS_Logo (1).png",
   "type": "image/png"
  }
 ],
 "rc5id": "20260304183456-58d18c8c-37f3-4e3a-9155-095957996722"
}

```
:::

# Code Blocks

Code blocks allow you to present **formatted code examples with syntax highlighting**.

They are ideal for:

* programming examples
* configuration snippets
* command-line instructions

**Notes**

* Specify the language after the triple backticks
* This enables syntax highlighting
* Use short examples to keep content readable

### Example

```py
# Python Example

def greet(name):
    return f"Hello {name}"

print(greet("Student"))
```

***

# Media Design Tips

### Use media intentionally

Avoid adding media that does not improve understanding.

### Keep file sizes reasonable

Large media files can slow down course loading.

### Combine media with layouts

Media works well inside:

* Tabs (multiple videos or images)
* Grids (side-by-side comparisons)
* Accordions (optional demonstrations)

### Provide context

Always introduce media with a short explanation so learners understand **why it is included**.

***

<table class="rc5-table"><thead><tr><th style="background-color: transparent">Media Type</th><th style="background-color: transparent">Purpose</th><th style="background-color: transparent">Best Use</th></tr></thead><tbody><tr><td style="background-color: transparent">Audio</td><td style="background-color: transparent">Recorded narration</td><td style="background-color: transparent">Lectures, feedback</td></tr><tr><td style="background-color: transparent">Video</td><td style="background-color: transparent">Demonstrations</td><td style="background-color: transparent">Tutorials</td></tr><tr><td style="background-color: transparent">Images</td><td style="background-color: transparent">Visual references</td><td style="background-color: transparent">Diagrams, screenshots</td></tr><tr><td style="background-color: transparent">Downloads</td><td style="background-color: transparent">Provide assets</td><td style="background-color: transparent">Labs, resources</td></tr><tr><td style="background-color: transparent">Code Blocks</td><td style="background-color: transparent">Display code</td><td style="background-color: transparent">Programming examples</td></tr></tbody></table>