{% from "userGuide/components/advanced.md" import slot_info_trigger, slot_type_info_trigger %}

## Modals

**Modals are to be used together with the [Trigger](#trigger) component for activation.**

<include src="codeAndOutput.md" boilerplate >
<variable name="highlightStyle">html</variable>
<variable name="code">
More about <trigger for="modal:loremipsum">trigger</trigger>.
<modal header="**Modal header** :rocket:" id="modal:loremipsum">
  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore
  magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
  consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
  Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
</modal>
<br>
This is the same <trigger for="modal:loremipsum">trigger</trigger> as last one.

<trigger for="modal:centered">This is a trigger for a centered modal</trigger>.

<modal header="**Centered** :rocket:" id="modal:centered" center>
  Centered
</modal>

<trigger for="modal:ok-text">This is a trigger for a modal with a custom OK button</trigger>.

<modal header="OK button visible!" id="modal:ok-text" ok-text="Custom OK">
  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore
  magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
  consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
  Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
</modal>
</variable>
</include>

<panel header="More about triggers">
<include src="extra/triggers.md" />
</panel><p/>

****Options****
Name | type | Default | Description
--- | --- | --- | ---
header{{slot_info_trigger}} | `String` | `''` | Header of the Modal component. Supports inline markdown text.
footer <hr style="margin-top:0.2rem; margin-bottom:0" /> <small>modal-footer <br> (deprecated)</small> | {{slot_type_info_trigger}} | empty | Specifying this will override the `ok-text` attribute, and the OK button will not render.
ok-text | `String` | `''` | Text for the OK button.
effect | `String` | `zoom` | Supports: `zoom`, `fade`.
id | `String` | | Used by [Trigger](#trigger) to activate the Modal by id.large | `Boolean` | `false` | Creates a [large Modal](https://getbootstrap.com/docs/4.0/components/modal/#optional-sizes).
small | `Boolean` | `false` | Creates a [small Modal](https://getbootstrap.com/docs/4.0/components/modal/#optional-sizes).
large | `Boolean` | `false` | Creates a [large Modal](https://getbootstrap.com/docs/4.0/components/modal/#optional-sizes).
center | `Boolean` | `false` | Vertically centers the modal (in addition to the horizontal centering by default).
backdrop | `Boolean` | `true` | Enables closing the Modal by clicking on the backdrop.

<span id="short" class="d-none">

```html
Click <trigger trigger="click" for="modal:unused">here</trigger> to open a modal.
<modal header="Modal header" id="modal:unused">
    Modal content
</modal>
```
</span>

<span id="examples" class="d-none">

Hover <trigger large for="modal:unused">here</trigger> to open a modal.
<modal header="Modal header" ok-text="OK" id="modal:unused">
  Modal content
</modal>
</span>
