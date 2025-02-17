## Embeds

**There are easy ways to embed media content such as YouTube videos and PowerPoint slides**.

###### Embedding Youtube Videos

Here are three ways of embedding YouTube videos and one example of how it will look in the page.

<!-- We use outputBox.md instead of codeAndOuput.md as boilerplate, because there are 3 ways to code vs 1 example -->
<include src="outputBox.md" boilerplate >
<span id="code">

```markdown
@[youtube](v40b3ExbM0c)
@[youtube](http://www.youtube.com/watch?v=v40b3ExbM0c)
@[youtube](http://youtu.be/v40b3ExbM0c)
```
</span>
<span id="output">

@[youtube](v40b3ExbM0c)
</span>
</include>

More media blocks, embedding services and additional options can be found in [Markdown-it documentation](https://github.com/rotorz/markdown-it-block-embed).

###### Embedding Powerpoint Slides (using the embed url from Powerpoint online)

Here is an example of embedding a PowerPoint slide deck:

<include src="codeAndOutput.md" boilerplate >
<variable name="highlightStyle">markdown</variable>
<variable name="code">
@[powerpoint](https://onedrive.live.com/embed?cid=A5AF047C4CAD67AB&resid=A5AF047C4CAD67AB%212070&authkey=&em=2)
</variable>
</include>

<span id="short" class="d-none">

```markdown
@[youtube](v40b3ExbM0c)
@[youtube](http://www.youtube.com/watch?v=v40b3ExbM0c)
@[youtube](http://youtu.be/v40b3ExbM0c)

@[powerpoint](https://onedrive.live.com/embed?cid=A5AF047C4CAD67AB&resid=A5AF047C4CAD67AB%212070&authkey=&em=2)
```
</span>

<span id="examples" class="d-none">

Embedded YouTube video:

@[youtube](v40b3ExbM0c)

Embedded slide deck:

@[powerpoint](https://onedrive.live.com/embed?cid=A5AF047C4CAD67AB&resid=A5AF047C4CAD67AB%212070&authkey=&em=2)

</span>