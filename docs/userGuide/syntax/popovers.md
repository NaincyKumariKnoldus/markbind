{% from "userGuide/components/advanced.md" import slot_info_trigger %}

## Popovers

<include src="codeAndOutput.md" boilerplate >
<variable name="highlightStyle">html</variable>
<variable name="code">
<popover content="Lorem ipsum dolor sit amet" placement="top">
  <button class="btn btn-secondary">Popover on top</button>
</popover>
<popover content="Lorem ipsum dolor sit amet" placement="left">
  <button class="btn btn-secondary">Popover on left</button>
</popover>
<popover content="Lorem ipsum dolor sit amet" placement="right">
  <button class="btn btn-secondary">Popover on right</button>
</popover>
<popover content="Lorem ipsum dolor sit amet" placement="bottom">
  <button class="btn btn-secondary">Popover on bottom</button>
</popover>
<hr>
<h4 class="no-index">Header</h4>
<popover header="Header" content="Lorem ipsum dolor sit amet" placement="top">
  <button class="btn btn-secondary">Popover on top</button>
</popover>
<popover header="Header" content="Lorem ipsum dolor sit amet" placement="left">
  <button class="btn btn-secondary">Popover on left</button>
</popover>
<popover header="Header" content="Lorem ipsum dolor sit amet" placement="right">
  <button class="btn btn-secondary">Popover on right</button>
</popover>
<popover header="Header" content="Lorem ipsum dolor sit amet" placement="bottom">
  <button class="btn btn-secondary">Popover on bottom</button>
</popover>
<hr />
<h4 class="no-index">Trigger</h4>
<p>
  <popover header="Header" content="Lorem ipsum dolor sit amet" placement="top" trigger="hover">
    <button class="btn btn-secondary">Mouseenter</button>
  </popover>
</p>
<h4 class="no-index">Markdown</h4>
<p>
  <popover header="**Emoji header** :rocket:" content="!!emoji!! content :cat:">
    <button class="btn btn-secondary">Hover</button>
  </popover>
</p>
<h4 class="no-index">Content using slot</h4>
<popover header="**Emoji header** :rocket:">
  <div slot="content">
    This is a long content...
  </div>
  <button class="btn btn-secondary">Hover</button>
</popover>
<br />
<br />
<h4 class="no-index">Wrap Text</h4>
<popover header="false" content="Nice!">What do you say</popover>
</variable>
</include>

**Using trigger for Popover:**<br>

<include src="codeAndOutput.md" boilerplate >
<variable name="highlightStyle">html</variable>
<variable name="code">
More about <trigger for="pop:trigger_id">trigger</trigger>.
<popover id="pop:trigger_id" content="This popover is triggered by a trigger"></popover>
<br>
This is the same <trigger for="pop:trigger_id">trigger</trigger> as last one.
</variable>
</include>

<panel header="More about triggers">
<include src="extra/triggers.md" />
</panel><p/>

****Options****

Name | Type | Default | Description
---- | ---- | ------- | ------
trigger | `String` |	`hover`	| How the Popover is triggered.<br>Supports: `click`, `focus`, `hover`.
header{{slot_info_trigger}} | `String` | `''` | Popover header, supports MarkDown text.
content{{slot_info_trigger}} | `String` | `''` | Popover content, supports MarkDown text.
placement | `String` | `top` | How to position the Popover.<br>Supports: `top`, `left`, `right`, `bottom`.


<span id="short" class="d-none">

```html
Hover over the <trigger for="pop:context-target">keyword</trigger> to see the popover.

<popover id="pop:context-target" header="Popover header" placement="top">
<div slot="content">

description :+1:

</div>
</popover>
```
</span>

<span id="examples" class="d-none">

Hover over the <trigger for="pop:context-target">keyword</trigger> to see the popover.

<popover id="pop:context-target" header="Popover header" placement="top">
<div slot="content">

description :+1:

</div>
</popover>
</span>
