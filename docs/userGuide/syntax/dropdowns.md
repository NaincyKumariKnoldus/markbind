{% from "userGuide/components/advanced.md" import slot_info_trigger %}

## Dropdowns

**While the main use case for dropdowns is under navbars, they can also be used as top-level components.**

<include src="codeAndOutput.md" boilerplate >
<variable name="highlightStyle">html</variable>
<variable name="code">
<!--Notice how header attribute supports inline MarkDown-->
<dropdown header="*Action*" type="primary">
  <li><a href="#dropdown" class="dropdown-item">Action</a></li>
  <li><a href="#dropdown" class="dropdown-item">Another action</a></li>
  <li><a href="#dropdown" class="dropdown-item">Something else here</a></li>
  <li role="separator" class="dropdown-divider"></li>
  <li><a href="#dropdown" class="dropdown-item">Separated link</a></li>
</dropdown>

<!-- For segmented dropdown, ignore header and add a "before" slot -->
<dropdown type="info">
  <button slot="before" type="button" class="btn btn-info">Segmented</button>
  <li><a href="#dropdown" class="dropdown-item">...</a></li>
</dropdown>

<!-- Right aligned list -->
<dropdown header="Right aligned list" type="primary" menu-align-right>
  <li><a href="#dropdown" class="dropdown-item">Something else here</a></li>
</dropdown>

<!-- Inside a bootstrap button group -->
<div class="btn-group d-flex mt-3" role="group">
  <a href="#dropdown" class="btn btn-danger w-100" role="button">Left</a>
  <!-- With slots you can handle some elements as native bootstrap -->
  <dropdown class="w-100">
    <button slot="button" type="button" class="btn btn-warning dropdown-toggle w-100">
      Action
      <span class="caret"></span>
    </button>
    <ul slot="dropdown-menu" class="dropdown-menu">
      <li><a href="#dropdown" class="dropdown-item">Action</a></li>
      <li><a href="#dropdown" class="dropdown-item">Another action</a></li>
      <li><a href="#dropdown" class="dropdown-item">Something else here</a></li>
      <li role="separator" class="dropdown-divider"></li>
      <li><a href="#dropdown" class="dropdown-item">Separated link</a></li>
    </ul>
  </dropdown>
  <a href="#dropdown" class="btn btn-success w-100" role="button">Right</a>
</div>
</variable>
</include>

**Dropdowns can also be nested within each other to create multi-level submenus.**

<include src="codeAndOutput.md" boilerplate >
<variable name="highlightStyle">html</variable>
<variable name="code">
<!-- Nest the dropdown syntax to create dropdown submenus -->
<dropdown header="*Multi-Level Dropdown*" type="primary">
  <li><a href="#dropdown" class="dropdown-item">Item</a></li>
  <li><a href="#dropdown" class="dropdown-item">Another item</a></li>
  <dropdown header="*Submenu*">
    <li><a href="#dropdown" class="dropdown-item">Item</a></li>
    <li><a href="#dropdown" class="dropdown-item">Another item</a></li>
  </dropdown>
</dropdown>
</variable>
</include>

****Options****

Name | Type | Default | Description
--- | --- | --- | ---
disabled | `Boolean` | `false` | Whether Dropdown can be opened.
menu-align-right | `Boolean` | `false` | Whether the dropdown list will be right-aligned.
header{{slot_info_trigger}} | `String` | `''` | Dropdown button header text. (Supports inline MarkDown syntax)
type | `String` | `default` | Supports: `default`, `primary`, `danger`, `info`, `warning`, `success`.

<div class="indented">

%%{{ icon_info }} You may refer to [this documentation](https://getbootstrap.com/docs/4.0/components/buttons/) regarding how you can use the **Bootstrap buttons**, and how to style them.%%
</div>


<span id="short" class="d-none">

```markdown
<dropdown header="Action" type="primary">
  <li><a href="#dropdown" class="dropdown-item">Action</a></li>
  <li><a href="#dropdown" class="dropdown-item">Another action</a></li>
  <li role="separator" class="dropdown-divider"></li>
  <li><a href="#dropdown" class="dropdown-item">Separated link</a></li>
</dropdown>
```
</span>

<span id="examples" class="d-none">

<dropdown header="Action" type="primary">
  <li><a href="#dropdown" class="dropdown-item">Action</a></li>
  <li><a href="#dropdown" class="dropdown-item">Another action</a></li>
  <li><a href="#dropdown" class="dropdown-item">Something else here</a></li>
  <li role="separator" class="dropdown-divider"></li>
  <li><a href="#dropdown" class="dropdown-item">Separated link</a></li>
</dropdown>

<!-- For segmented dropdown, ignore header and add a "before" slot -->
<dropdown type="info">
  <button slot="before" type="button" class="btn btn-info">Segmented</button>
  <li><a href="#dropdown" class="dropdown-item">...</a></li>
</dropdown>
<p/>
<!-- In a button group -->
<div class="btn-group d-flex" role="group">
  <a href="#dropdown" class="btn btn-danger w-100" role="button">Left</a>
  <!-- With slots you can handle some elements as native bootstrap -->
  <dropdown class="w-100">
    <button slot="button" type="button" class="btn btn-warning dropdown-toggle w-100">
      Action
      <span class="caret"></span>
    </button>
    <ul slot="dropdown-menu" class="dropdown-menu">
      <li><a href="#dropdown" class="dropdown-item">Action</a></li>
      <li><a href="#dropdown" class="dropdown-item">Another action</a></li>
      <li><a href="#dropdown" class="dropdown-item">Something else here</a></li>
      <li role="separator" class="dropdown-divider"></li>
      <li><a href="#dropdown" class="dropdown-item">Separated link</a></li>
    </ul>
  </dropdown>
  <a href="#dropdown" class="btn btn-success w-100" role="button">Right</a>
</div>
</span>
