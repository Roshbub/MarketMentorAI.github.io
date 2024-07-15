<!DOCTYPE html>

<html lang="en">
<head><meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>MarketMentorAI</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<style type="text/css">
    pre { line-height: 125%; }
td.linenos .normal { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
span.linenos { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
td.linenos .special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .pm { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation.Marker */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>
<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
  scrollbar-width: thin;
}

/* tiny scrollbar */

.jp-scrollbar-tiny::-webkit-scrollbar,
.jp-scrollbar-tiny::-webkit-scrollbar-corner {
  background-color: transparent;
  height: 4px;
  width: 4px;
}

.jp-scrollbar-tiny::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:horizontal {
  border-left: 0 solid transparent;
  border-right: 0 solid transparent;
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:vertical {
  border-top: 0 solid transparent;
  border-bottom: 0 solid transparent;
}

/*
 * Lumino
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
}

.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.lm-AccordionPanel[data-orientation='horizontal'] > .lm-AccordionPanel-title {
  /* Title is rotated for horizontal accordion panel using CSS */
  display: block;
  transform-origin: top left;
  transform: rotate(-90deg) translate(-100%);
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-CommandPalette-search {
  flex: 0 0 auto;
}

.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}

.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}

.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}

.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-close-icon {
  border: 1px solid transparent;
  background-color: transparent;
  position: absolute;
  z-index: 1;
  right: 3%;
  top: 0;
  bottom: 0;
  margin: auto;
  padding: 7px 0;
  display: none;
  vertical-align: middle;
  outline: 0;
  cursor: pointer;
}
.lm-close-icon:after {
  content: 'X';
  display: block;
  width: 15px;
  height: 15px;
  text-align: center;
  color: #000;
  font-weight: normal;
  font-size: 12px;
  cursor: pointer;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-DockPanel {
  z-index: 0;
}

.lm-DockPanel-widget {
  z-index: 0;
}

.lm-DockPanel-tabBar {
  z-index: 1;
}

.lm-DockPanel-handle {
  z-index: 2;
}

.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}

.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}

.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}

.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}

.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}

.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}

.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}

.lm-Menu-item {
  display: table-row;
}

.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}

.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}

.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}

.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}

.lm-MenuBar-item {
  box-sizing: border-box;
}

.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}

.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}

.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}

.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}

.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-SplitPanel-child {
  z-index: 0;
}

.lm-SplitPanel-handle {
  z-index: 1;
}

.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}

.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}

.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}

.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}

.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}

.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
  align-items: flex-end;
}

.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
  align-items: flex-end;
}

.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}

.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}

.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}

.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
  touch-action: none; /* Disable native Drag/Drop */
}

.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}

.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}

.lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing: border-box;
}

.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}

.lm-TabBar-addButton.lm-mod-hidden {
  display: none !important;
}

.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}

.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}

.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}

.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

.lm-TabBar-tabLabel .lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing: border-box;
  background: inherit;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-TabPanel-tabBar {
  z-index: 1;
}

.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
}

.jp-Collapse-header {
  padding: 1px 12px;
  background-color: var(--jp-layout-color1);
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  align-items: center;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  text-transform: uppercase;
  user-select: none;
}

.jp-Collapser-icon {
  height: 16px;
}

.jp-Collapse-header-collapsed .jp-Collapser-icon {
  transform: rotate(-90deg);
  margin: auto 0;
}

.jp-Collapser-title {
  line-height: 25px;
}

.jp-Collapse-contents {
  padding: 0 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add-above: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPGcgY2xpcC1wYXRoPSJ1cmwoI2NsaXAwXzEzN18xOTQ5MikiPgo8cGF0aCBjbGFzcz0ianAtaWNvbjMiIGQ9Ik00Ljc1IDQuOTMwNjZINi42MjVWNi44MDU2NkM2LjYyNSA3LjAxMTkxIDYuNzkzNzUgNy4xODA2NiA3IDcuMTgwNjZDNy4yMDYyNSA3LjE4MDY2IDcuMzc1IDcuMDExOTEgNy4zNzUgNi44MDU2NlY0LjkzMDY2SDkuMjVDOS40NTYyNSA0LjkzMDY2IDkuNjI1IDQuNzYxOTEgOS42MjUgNC41NTU2NkM5LjYyNSA0LjM0OTQxIDkuNDU2MjUgNC4xODA2NiA5LjI1IDQuMTgwNjZINy4zNzVWMi4zMDU2NkM3LjM3NSAyLjA5OTQxIDcuMjA2MjUgMS45MzA2NiA3IDEuOTMwNjZDNi43OTM3NSAxLjkzMDY2IDYuNjI1IDIuMDk5NDEgNi42MjUgMi4zMDU2NlY0LjE4MDY2SDQuNzVDNC41NDM3NSA0LjE4MDY2IDQuMzc1IDQuMzQ5NDEgNC4zNzUgNC41NTU2NkM0LjM3NSA0Ljc2MTkxIDQuNTQzNzUgNC45MzA2NiA0Ljc1IDQuOTMwNjZaIiBmaWxsPSIjNjE2MTYxIiBzdHJva2U9IiM2MTYxNjEiIHN0cm9rZS13aWR0aD0iMC43Ii8+CjwvZz4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTExLjUgOS41VjExLjVMMi41IDExLjVWOS41TDExLjUgOS41Wk0xMiA4QzEyLjU1MjMgOCAxMyA4LjQ0NzcyIDEzIDlWMTJDMTMgMTIuNTUyMyAxMi41NTIzIDEzIDEyIDEzTDIgMTNDMS40NDc3MiAxMyAxIDEyLjU1MjMgMSAxMlY5QzEgOC40NDc3MiAxLjQ0NzcxIDggMiA4TDEyIDhaIiBmaWxsPSIjNjE2MTYxIi8+CjxkZWZzPgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzEzN18xOTQ5MiI+CjxyZWN0IGNsYXNzPSJqcC1pY29uMyIgd2lkdGg9IjYiIGhlaWdodD0iNiIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0ibWF0cml4KC0xIDAgMCAxIDEwIDEuNTU1NjYpIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==);
  --jp-icon-add-below: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPGcgY2xpcC1wYXRoPSJ1cmwoI2NsaXAwXzEzN18xOTQ5OCkiPgo8cGF0aCBjbGFzcz0ianAtaWNvbjMiIGQ9Ik05LjI1IDEwLjA2OTNMNy4zNzUgMTAuMDY5M0w3LjM3NSA4LjE5NDM0QzcuMzc1IDcuOTg4MDkgNy4yMDYyNSA3LjgxOTM0IDcgNy44MTkzNEM2Ljc5Mzc1IDcuODE5MzQgNi42MjUgNy45ODgwOSA2LjYyNSA4LjE5NDM0TDYuNjI1IDEwLjA2OTNMNC43NSAxMC4wNjkzQzQuNTQzNzUgMTAuMDY5MyA0LjM3NSAxMC4yMzgxIDQuMzc1IDEwLjQ0NDNDNC4zNzUgMTAuNjUwNiA0LjU0Mzc1IDEwLjgxOTMgNC43NSAxMC44MTkzTDYuNjI1IDEwLjgxOTNMNi42MjUgMTIuNjk0M0M2LjYyNSAxMi45MDA2IDYuNzkzNzUgMTMuMDY5MyA3IDEzLjA2OTNDNy4yMDYyNSAxMy4wNjkzIDcuMzc1IDEyLjkwMDYgNy4zNzUgMTIuNjk0M0w3LjM3NSAxMC44MTkzTDkuMjUgMTAuODE5M0M5LjQ1NjI1IDEwLjgxOTMgOS42MjUgMTAuNjUwNiA5LjYyNSAxMC40NDQzQzkuNjI1IDEwLjIzODEgOS40NTYyNSAxMC4wNjkzIDkuMjUgMTAuMDY5M1oiIGZpbGw9IiM2MTYxNjEiIHN0cm9rZT0iIzYxNjE2MSIgc3Ryb2tlLXdpZHRoPSIwLjciLz4KPC9nPgo8cGF0aCBjbGFzcz0ianAtaWNvbjMiIGZpbGwtcnVsZT0iZXZlbm9kZCIgY2xpcC1ydWxlPSJldmVub2RkIiBkPSJNMi41IDUuNUwyLjUgMy41TDExLjUgMy41TDExLjUgNS41TDIuNSA1LjVaTTIgN0MxLjQ0NzcyIDcgMSA2LjU1MjI4IDEgNkwxIDNDMSAyLjQ0NzcyIDEuNDQ3NzIgMiAyIDJMMTIgMkMxMi41NTIzIDIgMTMgMi40NDc3MiAxMyAzTDEzIDZDMTMgNi41NTIyOSAxMi41NTIzIDcgMTIgN0wyIDdaIiBmaWxsPSIjNjE2MTYxIi8+CjxkZWZzPgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzEzN18xOTQ5OCI+CjxyZWN0IGNsYXNzPSJqcC1pY29uMyIgd2lkdGg9IjYiIGhlaWdodD0iNiIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0ibWF0cml4KDEgMS43NDg0NmUtMDcgMS43NDg0NmUtMDcgLTEgNCAxMy40NDQzKSIvPgo8L2NsaXBQYXRoPgo8L2RlZnM+Cjwvc3ZnPgo=);
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bell: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE2IDE2IiB2ZXJzaW9uPSIxLjEiPgogICA8cGF0aCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMzMzMzMzIgogICAgICBkPSJtOCAwLjI5Yy0xLjQgMC0yLjcgMC43My0zLjYgMS44LTEuMiAxLjUtMS40IDMuNC0xLjUgNS4yLTAuMTggMi4yLTAuNDQgNC0yLjMgNS4zbDAuMjggMS4zaDVjMC4wMjYgMC42NiAwLjMyIDEuMSAwLjcxIDEuNSAwLjg0IDAuNjEgMiAwLjYxIDIuOCAwIDAuNTItMC40IDAuNi0xIDAuNzEtMS41aDVsMC4yOC0xLjNjLTEuOS0wLjk3LTIuMi0zLjMtMi4zLTUuMy0wLjEzLTEuOC0wLjI2LTMuNy0xLjUtNS4yLTAuODUtMS0yLjItMS44LTMuNi0xLjh6bTAgMS40YzAuODggMCAxLjkgMC41NSAyLjUgMS4zIDAuODggMS4xIDEuMSAyLjcgMS4yIDQuNCAwLjEzIDEuNyAwLjIzIDMuNiAxLjMgNS4yaC0xMGMxLjEtMS42IDEuMi0zLjQgMS4zLTUuMiAwLjEzLTEuNyAwLjMtMy4zIDEuMi00LjQgMC41OS0wLjcyIDEuNi0xLjMgMi41LTEuM3ptLTAuNzQgMTJoMS41Yy0wLjAwMTUgMC4yOCAwLjAxNSAwLjc5LTAuNzQgMC43OS0wLjczIDAuMDAxNi0wLjcyLTAuNTMtMC43NC0wLjc5eiIgLz4KPC9zdmc+Cg==);
  --jp-icon-bug-dot: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiPgogICAgICAgIDxwYXRoIGZpbGwtcnVsZT0iZXZlbm9kZCIgY2xpcC1ydWxlPSJldmVub2RkIiBkPSJNMTcuMTkgOEgyMFYxMEgxNy45MUMxNy45NiAxMC4zMyAxOCAxMC42NiAxOCAxMVYxMkgyMFYxNEgxOC41SDE4VjE0LjAyNzVDMTUuNzUgMTQuMjc2MiAxNCAxNi4xODM3IDE0IDE4LjVDMTQgMTkuMjA4IDE0LjE2MzUgMTkuODc3OSAxNC40NTQ5IDIwLjQ3MzlDMTMuNzA2MyAyMC44MTE3IDEyLjg3NTcgMjEgMTIgMjFDOS43OCAyMSA3Ljg1IDE5Ljc5IDYuODEgMThINFYxNkg2LjA5QzYuMDQgMTUuNjcgNiAxNS4zNCA2IDE1VjE0SDRWMTJINlYxMUM2IDEwLjY2IDYuMDQgMTAuMzMgNi4wOSAxMEg0VjhINi44MUM3LjI2IDcuMjIgNy44OCA2LjU1IDguNjIgNi4wNEw3IDQuNDFMOC40MSAzTDEwLjU5IDUuMTdDMTEuMDQgNS4wNiAxMS41MSA1IDEyIDVDMTIuNDkgNSAxMi45NiA1LjA2IDEzLjQyIDUuMTdMMTUuNTkgM0wxNyA0LjQxTDE1LjM3IDYuMDRDMTYuMTIgNi41NSAxNi43NCA3LjIyIDE3LjE5IDhaTTEwIDE2SDE0VjE0SDEwVjE2Wk0xMCAxMkgxNFYxMEgxMFYxMloiIGZpbGw9IiM2MTYxNjEiLz4KICAgICAgICA8cGF0aCBkPSJNMjIgMTguNUMyMiAyMC40MzMgMjAuNDMzIDIyIDE4LjUgMjJDMTYuNTY3IDIyIDE1IDIwLjQzMyAxNSAxOC41QzE1IDE2LjU2NyAxNi41NjcgMTUgMTguNSAxNUMyMC40MzMgMTUgMjIgMTYuNTY3IDIyIDE4LjVaIiBmaWxsPSIjNjE2MTYxIi8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0yMCA4aC0yLjgxYy0uNDUtLjc4LTEuMDctMS40NS0xLjgyLTEuOTZMMTcgNC40MSAxNS41OSAzbC0yLjE3IDIuMTdDMTIuOTYgNS4wNiAxMi40OSA1IDEyIDVjLS40OSAwLS45Ni4wNi0xLjQxLjE3TDguNDEgMyA3IDQuNDFsMS42MiAxLjYzQzcuODggNi41NSA3LjI2IDcuMjIgNi44MSA4SDR2MmgyLjA5Yy0uMDUuMzMtLjA5LjY2LS4wOSAxdjFINHYyaDJ2MWMwIC4zNC4wNC42Ny4wOSAxSDR2MmgyLjgxYzEuMDQgMS43OSAyLjk3IDMgNS4xOSAzczQuMTUtMS4yMSA1LjE5LTNIMjB2LTJoLTIuMDljLjA1LS4zMy4wOS0uNjYuMDktMXYtMWgydi0yaC0ydi0xYzAtLjM0LS4wNC0uNjctLjA5LTFIMjBWOHptLTYgOGgtNHYtMmg0djJ6bTAtNGgtNHYtMmg0djJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik05IDE2LjE3TDQuODMgMTJsLTEuNDIgMS40MUw5IDE5IDIxIDdsLTEuNDEtMS40MXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBzaGFwZS1yZW5kZXJpbmc9Imdlb21ldHJpY1ByZWNpc2lvbiI+CiAgICA8cGF0aCBkPSJNNi41OSwzLjQxTDIsOEw2LjU5LDEyLjZMOCwxMS4xOEw0LjgyLDhMOCw0LjgyTDYuNTksMy40MU0xMi40MSwzLjQxTDExLDQuODJMMTQuMTgsOEwxMSwxMS4xOEwxMi40MSwxMi42TDE3LDhMMTIuNDEsMy40MU0yMS41OSwxMS41OUwxMy41LDE5LjY4TDkuODMsMTZMOC40MiwxNy40MUwxMy41LDIyLjVMMjMsMTNMMjEuNTksMTEuNTlaIiAvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTExLjQgMTguNkw2LjggMTRMMTEuNCA5LjRMMTAgOEw0IDE0TDEwIDIwTDExLjQgMTguNlpNMTYuNiAxOC42TDIxLjIgMTRMMTYuNiA5LjRMMTggOEwyNCAxNEwxOCAyMEwxNi42IDE4LjZWMTguNloiLz4KCTwvZz4KPC9zdmc+Cg==);
  --jp-icon-collapse-all: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTggMmMxIDAgMTEgMCAxMiAwczIgMSAyIDJjMCAxIDAgMTEgMCAxMnMwIDItMiAyQzIwIDE0IDIwIDQgMjAgNFMxMCA0IDYgNGMwLTIgMS0yIDItMnoiIC8+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTE4IDhjMC0xLTEtMi0yLTJTNSA2IDQgNnMtMiAxLTIgMmMwIDEgMCAxMSAwIDEyczEgMiAyIDJjMSAwIDExIDAgMTIgMHMyLTEgMi0yYzAtMSAwLTExIDAtMTJ6bS0yIDB2MTJINFY4eiIgLz4KICAgICAgICA8cGF0aCBkPSJNNiAxM3YyaDh2LTJ6IiAvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1jb25zb2xlLWljb24tYmFja2dyb3VuZC1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtY29uc29sZS1pY29uLWNvbG9yIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIj4KICAgIDxwYXRoIGQ9Ik0xMDUgMTI3LjNoNDB2MTIuOGgtNDB6TTUxLjEgNzdMNzQgOTkuOWwtMjMuMyAyMy4zIDEwLjUgMTAuNSAyMy4zLTIzLjNMOTUgOTkuOSA4NC41IDg5LjQgNjEuNiA2Ni41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-copyright: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDI0IDI0IiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCI+CiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0xMS44OCw5LjE0YzEuMjgsMC4wNiwxLjYxLDEuMTUsMS42MywxLjY2aDEuNzljLTAuMDgtMS45OC0xLjQ5LTMuMTktMy40NS0zLjE5QzkuNjQsNy42MSw4LDksOCwxMi4xNCBjMCwxLjk0LDAuOTMsNC4yNCwzLjg0LDQuMjRjMi4yMiwwLDMuNDEtMS42NSwzLjQ0LTIuOTVoLTEuNzljLTAuMDMsMC41OS0wLjQ1LDEuMzgtMS42MywxLjQ0QzEwLjU1LDE0LjgzLDEwLDEzLjgxLDEwLDEyLjE0IEMxMCw5LjI1LDExLjI4LDkuMTYsMTEuODgsOS4xNHogTTEyLDJDNi40OCwyLDIsNi40OCwyLDEyczQuNDgsMTAsMTAsMTBzMTAtNC40OCwxMC0xMFMxNy41MiwyLDEyLDJ6IE0xMiwyMGMtNC40MSwwLTgtMy41OS04LTggczMuNTktOCw4LThzOCwzLjU5LDgsOFMxNi40MSwyMCwxMiwyMHoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-delete: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2cHgiIGhlaWdodD0iMTZweCI+CiAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIiAvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjI2MjYyIiBkPSJNNiAxOWMwIDEuMS45IDIgMiAyaDhjMS4xIDAgMi0uOSAyLTJWN0g2djEyek0xOSA0aC0zLjVsLTEtMWgtNWwtMSAxSDV2MmgxNFY0eiIgLz4KPC9zdmc+Cg==);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-duplicate: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTIuNzk5OTggMC44NzVIOC44OTU4MkM5LjIwMDYxIDAuODc1IDkuNDQ5OTggMS4xMzkxNCA5LjQ0OTk4IDEuNDYxOThDOS40NDk5OCAxLjc4NDgyIDkuMjAwNjEgMi4wNDg5NiA4Ljg5NTgyIDIuMDQ4OTZIMy4zNTQxNUMzLjA0OTM2IDIuMDQ4OTYgMi43OTk5OCAyLjMxMzEgMi43OTk5OCAyLjYzNTk0VjkuNjc5NjlDMi43OTk5OCAxMC4wMDI1IDIuNTUwNjEgMTAuMjY2NyAyLjI0NTgyIDEwLjI2NjdDMS45NDEwMyAxMC4yNjY3IDEuNjkxNjUgMTAuMDAyNSAxLjY5MTY1IDkuNjc5NjlWMi4wNDg5NkMxLjY5MTY1IDEuNDAzMjggMi4xOTA0IDAuODc1IDIuNzk5OTggMC44NzVaTTUuMzY2NjUgMTEuOVY0LjU1SDExLjA4MzNWMTEuOUg1LjM2NjY1Wk00LjE0MTY1IDQuMTQxNjdDNC4xNDE2NSAzLjY5MDYzIDQuNTA3MjggMy4zMjUgNC45NTgzMiAzLjMyNUgxMS40OTE3QzExLjk0MjcgMy4zMjUgMTIuMzA4MyAzLjY5MDYzIDEyLjMwODMgNC4xNDE2N1YxMi4zMDgzQzEyLjMwODMgMTIuNzU5NCAxMS45NDI3IDEzLjEyNSAxMS40OTE3IDEzLjEyNUg0Ljk1ODMyQzQuNTA3MjggMTMuMTI1IDQuMTQxNjUgMTIuNzU5NCA0LjE0MTY1IDEyLjMwODNWNC4xNDE2N1oiIGZpbGw9IiM2MTYxNjEiLz4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBkPSJNOS40MzU3NCA4LjI2NTA3SDguMzY0MzFWOS4zMzY1QzguMzY0MzEgOS40NTQzNSA4LjI2Nzg4IDkuNTUwNzggOC4xNTAwMiA5LjU1MDc4QzguMDMyMTcgOS41NTA3OCA3LjkzNTc0IDkuNDU0MzUgNy45MzU3NCA5LjMzNjVWOC4yNjUwN0g2Ljg2NDMxQzYuNzQ2NDUgOC4yNjUwNyA2LjY1MDAyIDguMTY4NjQgNi42NTAwMiA4LjA1MDc4QzYuNjUwMDIgNy45MzI5MiA2Ljc0NjQ1IDcuODM2NSA2Ljg2NDMxIDcuODM2NUg3LjkzNTc0VjYuNzY1MDdDNy45MzU3NCA2LjY0NzIxIDguMDMyMTcgNi41NTA3OCA4LjE1MDAyIDYuNTUwNzhDOC4yNjc4OCA2LjU1MDc4IDguMzY0MzEgNi42NDcyMSA4LjM2NDMxIDYuNzY1MDdWNy44MzY1SDkuNDM1NzRDOS41NTM2IDcuODM2NSA5LjY1MDAyIDcuOTMyOTIgOS42NTAwMiA4LjA1MDc4QzkuNjUwMDIgOC4xNjg2NCA5LjU1MzYgOC4yNjUwNyA5LjQzNTc0IDguMjY1MDdaIiBmaWxsPSIjNjE2MTYxIiBzdHJva2U9IiM2MTYxNjEiIHN0cm9rZS13aWR0aD0iMC41Ii8+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-error: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj48Y2lyY2xlIGN4PSIxMiIgY3k9IjE5IiByPSIyIi8+PHBhdGggZD0iTTEwIDNoNHYxMmgtNHoiLz48L2c+CjxwYXRoIGZpbGw9Im5vbmUiIGQ9Ik0wIDBoMjR2MjRIMHoiLz4KPC9zdmc+Cg==);
  --jp-icon-expand-all: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTggMmMxIDAgMTEgMCAxMiAwczIgMSAyIDJjMCAxIDAgMTEgMCAxMnMwIDItMiAyQzIwIDE0IDIwIDQgMjAgNFMxMCA0IDYgNGMwLTIgMS0yIDItMnoiIC8+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTE4IDhjMC0xLTEtMi0yLTJTNSA2IDQgNnMtMiAxLTIgMmMwIDEgMCAxMSAwIDEyczEgMiAyIDJjMSAwIDExIDAgMTIgMHMyLTEgMi0yYzAtMSAwLTExIDAtMTJ6bS0yIDB2MTJINFY4eiIgLz4KICAgICAgICA8cGF0aCBkPSJNMTEgMTBIOXYzSDZ2MmgzdjNoMnYtM2gzdi0yaC0zeiIgLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-dot: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTE0LDEyVjE5Ljg4QzE0LjA0LDIwLjE4IDEzLjk0LDIwLjUgMTMuNzEsMjAuNzFDMTMuMzIsMjEuMSAxMi42OSwyMS4xIDEyLjMsMjAuNzFMMTAuMjksMTguN0MxMC4wNiwxOC40NyA5Ljk2LDE4LjE2IDEwLDE3Ljg3VjEySDkuOTdMNC4yMSw0LjYyQzMuODcsNC4xOSAzLjk1LDMuNTYgNC4zOCwzLjIyQzQuNTcsMy4wOCA0Ljc4LDMgNSwzVjNIMTlWM0MxOS4yMiwzIDE5LjQzLDMuMDggMTkuNjIsMy4yMkMyMC4wNSwzLjU2IDIwLjEzLDQuMTkgMTkuNzksNC42MkwxNC4wMywxMkgxNFoiIC8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWRvdCIgZmlsbD0iI0ZGRiI+CiAgICA8Y2lyY2xlIGN4PSIxOCIgY3k9IjE3IiByPSIzIj48L2NpcmNsZT4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-filter: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTE0LDEyVjE5Ljg4QzE0LjA0LDIwLjE4IDEzLjk0LDIwLjUgMTMuNzEsMjAuNzFDMTMuMzIsMjEuMSAxMi42OSwyMS4xIDEyLjMsMjAuNzFMMTAuMjksMTguN0MxMC4wNiwxOC40NyA5Ljk2LDE4LjE2IDEwLDE3Ljg3VjEySDkuOTdMNC4yMSw0LjYyQzMuODcsNC4xOSAzLjk1LDMuNTYgNC4zOCwzLjIyQzQuNTcsMy4wOCA0Ljc4LDMgNSwzVjNIMTlWM0MxOS4yMiwzIDE5LjQzLDMuMDggMTkuNjIsMy4yMkMyMC4wNSwzLjU2IDIwLjEzLDQuMTkgMTkuNzksNC42MkwxNC4wMywxMkgxNFoiIC8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-folder-favorite: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjRweCIgZmlsbD0iIzAwMDAwMCI+CiAgPHBhdGggZD0iTTAgMGgyNHYyNEgwVjB6IiBmaWxsPSJub25lIi8+PHBhdGggY2xhc3M9ImpwLWljb24zIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxNjE2MSIgZD0iTTIwIDZoLThsLTItMkg0Yy0xLjEgMC0yIC45LTIgMnYxMmMwIDEuMS45IDIgMiAyaDE2YzEuMSAwIDItLjkgMi0yVjhjMC0xLjEtLjktMi0yLTJ6bS0yLjA2IDExTDE1IDE1LjI4IDEyLjA2IDE3bC43OC0zLjMzLTIuNTktMi4yNCAzLjQxLS4yOUwxNSA4bDEuMzQgMy4xNCAzLjQxLjI5LTIuNTkgMi4yNC43OCAzLjMzeiIvPgo8L3N2Zz4K);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-home: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjRweCIgZmlsbD0iIzAwMDAwMCI+CiAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjxwYXRoIGNsYXNzPSJqcC1pY29uMyBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xMCAyMHYtNmg0djZoNXYtOGgzTDEyIDMgMiAxMmgzdjh6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-info: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUwLjk3OCA1MC45NzgiPgoJPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KCQk8cGF0aCBkPSJNNDMuNTIsNy40NThDMzguNzExLDIuNjQ4LDMyLjMwNywwLDI1LjQ4OSwwQzE4LjY3LDAsMTIuMjY2LDIuNjQ4LDcuNDU4LDcuNDU4CgkJCWMtOS45NDMsOS45NDEtOS45NDMsMjYuMTE5LDAsMzYuMDYyYzQuODA5LDQuODA5LDExLjIxMiw3LjQ1NiwxOC4wMzEsNy40NThjMCwwLDAuMDAxLDAsMC4wMDIsMAoJCQljNi44MTYsMCwxMy4yMjEtMi42NDgsMTguMDI5LTcuNDU4YzQuODA5LTQuODA5LDcuNDU3LTExLjIxMiw3LjQ1Ny0xOC4wM0M1MC45NzcsMTguNjcsNDguMzI4LDEyLjI2Niw0My41Miw3LjQ1OHoKCQkJIE00Mi4xMDYsNDIuMTA1Yy00LjQzMiw0LjQzMS0xMC4zMzIsNi44NzItMTYuNjE1LDYuODcyaC0wLjAwMmMtNi4yODUtMC4wMDEtMTIuMTg3LTIuNDQxLTE2LjYxNy02Ljg3MgoJCQljLTkuMTYyLTkuMTYzLTkuMTYyLTI0LjA3MSwwLTMzLjIzM0MxMy4zMDMsNC40NCwxOS4yMDQsMiwyNS40ODksMmM2LjI4NCwwLDEyLjE4NiwyLjQ0LDE2LjYxNyw2Ljg3MgoJCQljNC40MzEsNC40MzEsNi44NzEsMTAuMzMyLDYuODcxLDE2LjYxN0M0OC45NzcsMzEuNzcyLDQ2LjUzNiwzNy42NzUsNDIuMTA2LDQyLjEwNXoiLz4KCQk8cGF0aCBkPSJNMjMuNTc4LDMyLjIxOGMtMC4wMjMtMS43MzQsMC4xNDMtMy4wNTksMC40OTYtMy45NzJjMC4zNTMtMC45MTMsMS4xMS0xLjk5NywyLjI3Mi0zLjI1MwoJCQljMC40NjgtMC41MzYsMC45MjMtMS4wNjIsMS4zNjctMS41NzVjMC42MjYtMC43NTMsMS4xMDQtMS40NzgsMS40MzYtMi4xNzVjMC4zMzEtMC43MDcsMC40OTUtMS41NDEsMC40OTUtMi41CgkJCWMwLTEuMDk2LTAuMjYtMi4wODgtMC43NzktMi45NzljLTAuNTY1LTAuODc5LTEuNTAxLTEuMzM2LTIuODA2LTEuMzY5Yy0xLjgwMiwwLjA1Ny0yLjk4NSwwLjY2Ny0zLjU1LDEuODMyCgkJCWMtMC4zMDEsMC41MzUtMC41MDMsMS4xNDEtMC42MDcsMS44MTRjLTAuMTM5LDAuNzA3LTAuMjA3LDEuNDMyLTAuMjA3LDIuMTc0aC0yLjkzN2MtMC4wOTEtMi4yMDgsMC40MDctNC4xMTQsMS40OTMtNS43MTkKCQkJYzEuMDYyLTEuNjQsMi44NTUtMi40ODEsNS4zNzgtMi41MjdjMi4xNiwwLjAyMywzLjg3NCwwLjYwOCw1LjE0MSwxLjc1OGMxLjI3OCwxLjE2LDEuOTI5LDIuNzY0LDEuOTUsNC44MTEKCQkJYzAsMS4xNDItMC4xMzcsMi4xMTEtMC40MSwyLjkxMWMtMC4zMDksMC44NDUtMC43MzEsMS41OTMtMS4yNjgsMi4yNDNjLTAuNDkyLDAuNjUtMS4wNjgsMS4zMTgtMS43MywyLjAwMgoJCQljLTAuNjUsMC42OTctMS4zMTMsMS40NzktMS45ODcsMi4zNDZjLTAuMjM5LDAuMzc3LTAuNDI5LDAuNzc3LTAuNTY1LDEuMTk5Yy0wLjE2LDAuOTU5LTAuMjE3LDEuOTUxLTAuMTcxLDIuOTc5CgkJCUMyNi41ODksMzIuMjE4LDIzLjU3OCwzMi4yMTgsMjMuNTc4LDMyLjIxOHogTTIzLjU3OCwzOC4yMnYtMy40ODRoMy4wNzZ2My40ODRIMjMuNTc4eiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaW5zcGVjdG9yLWljb24tY29sb3IganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtanNvbi1pY29uLWNvbG9yIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0Y5QTgyNSI+CiAgICA8cGF0aCBkPSJNMjAuMiAxMS44Yy0xLjYgMC0xLjcuNS0xLjcgMSAwIC40LjEuOS4xIDEuMy4xLjUuMS45LjEgMS4zIDAgMS43LTEuNCAyLjMtMy41IDIuM2gtLjl2LTEuOWguNWMxLjEgMCAxLjQgMCAxLjQtLjggMC0uMyAwLS42LS4xLTEgMC0uNC0uMS0uOC0uMS0xLjIgMC0xLjMgMC0xLjggMS4zLTItMS4zLS4yLTEuMy0uNy0xLjMtMiAwLS40LjEtLjguMS0xLjIuMS0uNC4xLS43LjEtMSAwLS44LS40LS43LTEuNC0uOGgtLjVWNC4xaC45YzIuMiAwIDMuNS43IDMuNSAyLjMgMCAuNC0uMS45LS4xIDEuMy0uMS41LS4xLjktLjEgMS4zIDAgLjUuMiAxIDEuNyAxdjEuOHpNMS44IDEwLjFjMS42IDAgMS43LS41IDEuNy0xIDAtLjQtLjEtLjktLjEtMS4zLS4xLS41LS4xLS45LS4xLTEuMyAwLTEuNiAxLjQtMi4zIDMuNS0yLjNoLjl2MS45aC0uNWMtMSAwLTEuNCAwLTEuNC44IDAgLjMgMCAuNi4xIDEgMCAuMi4xLjYuMSAxIDAgMS4zIDAgMS44LTEuMyAyQzYgMTEuMiA2IDExLjcgNiAxM2MwIC40LS4xLjgtLjEgMS4yLS4xLjMtLjEuNy0uMSAxIDAgLjguMy44IDEuNC44aC41djEuOWgtLjljLTIuMSAwLTMuNS0uNi0zLjUtMi4zIDAtLjQuMS0uOS4xLTEuMy4xLS41LjEtLjkuMS0xLjMgMC0uNS0uMi0xLTEuNy0xdi0xLjl6Ii8+CiAgICA8Y2lyY2xlIGN4PSIxMSIgY3k9IjEzLjgiIHI9IjIuMSIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSI4LjIiIHI9IjIuMSIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-julia: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDMyNSAzMDAiPgogIDxnIGNsYXNzPSJqcC1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjY2IzYzMzIj4KICAgIDxwYXRoIGQ9Ik0gMTUwLjg5ODQzOCAyMjUgQyAxNTAuODk4NDM4IDI2Ni40MjE4NzUgMTE3LjMyMDMxMiAzMDAgNzUuODk4NDM4IDMwMCBDIDM0LjQ3NjU2MiAzMDAgMC44OTg0MzggMjY2LjQyMTg3NSAwLjg5ODQzOCAyMjUgQyAwLjg5ODQzOCAxODMuNTc4MTI1IDM0LjQ3NjU2MiAxNTAgNzUuODk4NDM4IDE1MCBDIDExNy4zMjAzMTIgMTUwIDE1MC44OTg0MzggMTgzLjU3ODEyNSAxNTAuODk4NDM4IDIyNSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzM4OTgyNiI+CiAgICA8cGF0aCBkPSJNIDIzNy41IDc1IEMgMjM3LjUgMTE2LjQyMTg3NSAyMDMuOTIxODc1IDE1MCAxNjIuNSAxNTAgQyAxMjEuMDc4MTI1IDE1MCA4Ny41IDExNi40MjE4NzUgODcuNSA3NSBDIDg3LjUgMzMuNTc4MTI1IDEyMS4wNzgxMjUgMCAxNjIuNSAwIEMgMjAzLjkyMTg3NSAwIDIzNy41IDMzLjU3ODEyNSAyMzcuNSA3NSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzk1NThiMiI+CiAgICA8cGF0aCBkPSJNIDMyNC4xMDE1NjIgMjI1IEMgMzI0LjEwMTU2MiAyNjYuNDIxODc1IDI5MC41MjM0MzggMzAwIDI0OS4xMDE1NjIgMzAwIEMgMjA3LjY3OTY4OCAzMDAgMTc0LjEwMTU2MiAyNjYuNDIxODc1IDE3NC4xMDE1NjIgMjI1IEMgMTc0LjEwMTU2MiAxODMuNTc4MTI1IDIwNy42Nzk2ODggMTUwIDI0OS4xMDE1NjIgMTUwIEMgMjkwLjUyMzQzOCAxNTAgMzI0LjEwMTU2MiAxODMuNTc4MTI1IDMyNC4xMDE1NjIgMjI1Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgPGcgY2xhc3M9ImpwLWp1cHl0ZXItaWNvbi1jb2xvciIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgIDxnIGNsYXNzPSJqcC1qdXB5dGVyLWljb24tY29sb3IiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launch: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMzIgMzIiIHdpZHRoPSIzMiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0yNiwyOEg2YTIuMDAyNywyLjAwMjcsMCwwLDEtMi0yVjZBMi4wMDI3LDIuMDAyNywwLDAsMSw2LDRIMTZWNkg2VjI2SDI2VjE2aDJWMjZBMi4wMDI3LDIuMDAyNywwLDAsMSwyNiwyOFoiLz4KICAgIDxwb2x5Z29uIHBvaW50cz0iMjAgMiAyMCA0IDI2LjU4NiA0IDE4IDEyLjU4NiAxOS40MTQgMTQgMjggNS40MTQgMjggMTIgMzAgMTIgMzAgMiAyMCAyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4K);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-move-down: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBkPSJNMTIuNDcxIDcuNTI4OTlDMTIuNzYzMiA3LjIzNjg0IDEyLjc2MzIgNi43NjMxNiAxMi40NzEgNi40NzEwMVY2LjQ3MTAxQzEyLjE3OSA2LjE3OTA1IDExLjcwNTcgNi4xNzg4NCAxMS40MTM1IDYuNDcwNTRMNy43NSAxMC4xMjc1VjEuNzVDNy43NSAxLjMzNTc5IDcuNDE0MjEgMSA3IDFWMUM2LjU4NTc5IDEgNi4yNSAxLjMzNTc5IDYuMjUgMS43NVYxMC4xMjc1TDIuNTk3MjYgNi40NjgyMkMyLjMwMzM4IDYuMTczODEgMS44MjY0MSA2LjE3MzU5IDEuNTMyMjYgNi40Njc3NFY2LjQ2Nzc0QzEuMjM4MyA2Ljc2MTcgMS4yMzgzIDcuMjM4MyAxLjUzMjI2IDcuNTMyMjZMNi4yOTI4OSAxMi4yOTI5QzYuNjgzNDIgMTIuNjgzNCA3LjMxNjU4IDEyLjY4MzQgNy43MDcxMSAxMi4yOTI5TDEyLjQ3MSA3LjUyODk5WiIgZmlsbD0iIzYxNjE2MSIvPgo8L3N2Zz4K);
  --jp-icon-move-up: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBkPSJNMS41Mjg5OSA2LjQ3MTAxQzEuMjM2ODQgNi43NjMxNiAxLjIzNjg0IDcuMjM2ODQgMS41Mjg5OSA3LjUyODk5VjcuNTI4OTlDMS44MjA5NSA3LjgyMDk1IDIuMjk0MjYgNy44MjExNiAyLjU4NjQ5IDcuNTI5NDZMNi4yNSAzLjg3MjVWMTIuMjVDNi4yNSAxMi42NjQyIDYuNTg1NzkgMTMgNyAxM1YxM0M3LjQxNDIxIDEzIDcuNzUgMTIuNjY0MiA3Ljc1IDEyLjI1VjMuODcyNUwxMS40MDI3IDcuNTMxNzhDMTEuNjk2NiA3LjgyNjE5IDEyLjE3MzYgNy44MjY0MSAxMi40Njc3IDcuNTMyMjZWNy41MzIyNkMxMi43NjE3IDcuMjM4MyAxMi43NjE3IDYuNzYxNyAxMi40Njc3IDYuNDY3NzRMNy43MDcxMSAxLjcwNzExQzcuMzE2NTggMS4zMTY1OCA2LjY4MzQyIDEuMzE2NTggNi4yOTI4OSAxLjcwNzExTDEuNTI4OTkgNi40NzEwMVoiIGZpbGw9IiM2MTYxNjEiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtbm90ZWJvb2staWNvbi1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-numbering: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTQgMTlINlYxOS41SDVWMjAuNUg2VjIxSDRWMjJIN1YxOEg0VjE5Wk01IDEwSDZWNkg0VjdINVYxMFpNNCAxM0g1LjhMNCAxNS4xVjE2SDdWMTVINS4yTDcgMTIuOVYxMkg0VjEzWk05IDdWOUgyM1Y3SDlaTTkgMjFIMjNWMTlIOVYyMVpNOSAxNUgyM1YxM0g5VjE1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-offline-bolt: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDIuMDJjLTUuNTEgMC05Ljk4IDQuNDctOS45OCA5Ljk4czQuNDcgOS45OCA5Ljk4IDkuOTggOS45OC00LjQ3IDkuOTgtOS45OFMxNy41MSAyLjAyIDEyIDIuMDJ6TTExLjQ4IDIwdi02LjI2SDhMMTMgNHY2LjI2aDMuMzVMMTEuNDggMjB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-pdf: url(data:image/svg+xml;base64,PHN2ZwogICB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyMiAyMiIgd2lkdGg9IjE2Ij4KICAgIDxwYXRoIHRyYW5zZm9ybT0icm90YXRlKDQ1KSIgY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0ZGMkEyQSIKICAgICAgIGQ9Im0gMjIuMzQ0MzY5LC0zLjAxNjM2NDIgaCA1LjYzODYwNCB2IDEuNTc5MjQzMyBoIC0zLjU0OTIyNyB2IDEuNTA4NjkyOTkgaCAzLjMzNzU3NiBWIDEuNjUwODE1NCBoIC0zLjMzNzU3NiB2IDMuNDM1MjYxMyBoIC0yLjA4OTM3NyB6IG0gLTcuMTM2NDQ0LDEuNTc5MjQzMyB2IDQuOTQzOTU0MyBoIDAuNzQ4OTIgcSAxLjI4MDc2MSwwIDEuOTUzNzAzLC0wLjYzNDk1MzUgMC42NzgzNjksLTAuNjM0OTUzNSAwLjY3ODM2OSwtMS44NDUxNjQxIDAsLTEuMjA0NzgzNTUgLTAuNjcyOTQyLC0xLjgzNDMxMDExIC0wLjY3Mjk0MiwtMC42Mjk1MjY1OSAtMS45NTkxMywtMC42Mjk1MjY1OSB6IG0gLTIuMDg5Mzc3LC0xLjU3OTI0MzMgaCAyLjIwMzM0MyBxIDEuODQ1MTY0LDAgMi43NDYwMzksMC4yNjU5MjA3IDAuOTA2MzAxLDAuMjYwNDkzNyAxLjU1MjEwOCwwLjg5MDAyMDMgMC41Njk4MywwLjU0ODEyMjMgMC44NDY2MDUsMS4yNjQ0ODAwNiAwLjI3Njc3NCwwLjcxNjM1NzgxIDAuMjc2Nzc0LDEuNjIyNjU4OTQgMCwwLjkxNzE1NTEgLTAuMjc2Nzc0LDEuNjM4OTM5OSAtMC4yNzY3NzUsMC43MTYzNTc4IC0wLjg0NjYwNSwxLjI2NDQ4IC0wLjY1MTIzNCwwLjYyOTUyNjYgLTEuNTYyOTYyLDAuODk1NDQ3MyAtMC45MTE3MjgsMC4yNjA0OTM3IC0yLjczNTE4NSwwLjI2MDQ5MzcgaCAtMi4yMDMzNDMgeiBtIC04LjE0NTg1NjUsMCBoIDMuNDY3ODIzIHEgMS41NDY2ODE2LDAgMi4zNzE1Nzg1LDAuNjg5MjIzIDAuODMwMzI0LDAuNjgzNzk2MSAwLjgzMDMyNCwxLjk1MzcwMzE0IDAsMS4yNzUzMzM5NyAtMC44MzAzMjQsMS45NjQ1NTcwNiBRIDkuOTg3MTk2MSwyLjI3NDkxNSA4LjQ0MDUxNDUsMi4yNzQ5MTUgSCA3LjA2MjA2ODQgViA1LjA4NjA3NjcgSCA0Ljk3MjY5MTUgWiBtIDIuMDg5Mzc2OSwxLjUxNDExOTkgdiAyLjI2MzAzOTQzIGggMS4xNTU5NDEgcSAwLjYwNzgxODgsMCAwLjkzODg2MjksLTAuMjkzMDU1NDcgMC4zMzEwNDQxLC0wLjI5ODQ4MjQxIDAuMzMxMDQ0MSwtMC44NDExNzc3MiAwLC0wLjU0MjY5NTMxIC0wLjMzMTA0NDEsLTAuODM1NzUwNzQgLTAuMzMxMDQ0MSwtMC4yOTMwNTU1IC0wLjkzODg2MjksLTAuMjkzMDU1NSB6IgovPgo8L3N2Zz4K);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iLTEwIC0xMCAxMzEuMTYxMzYxNjk0MzM1OTQgMTMyLjM4ODk5OTkzODk2NDg0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMzA2OTk4IiBkPSJNIDU0LjkxODc4NSw5LjE5Mjc0MjFlLTQgQyA1MC4zMzUxMzIsMC4wMjIyMTcyNyA0NS45NTc4NDYsMC40MTMxMzY5NyA0Mi4xMDYyODUsMS4wOTQ2NjkzIDMwLjc2MDA2OSwzLjA5OTE3MzEgMjguNzAwMDM2LDcuMjk0NzcxNCAyOC43MDAwMzUsMTUuMDMyMTY5IHYgMTAuMjE4NzUgaCAyNi44MTI1IHYgMy40MDYyNSBoIC0yNi44MTI1IC0xMC4wNjI1IGMgLTcuNzkyNDU5LDAgLTE0LjYxNTc1ODgsNC42ODM3MTcgLTE2Ljc0OTk5OTgsMTMuNTkzNzUgLTIuNDYxODE5OTgsMTAuMjEyOTY2IC0yLjU3MTAxNTA4LDE2LjU4NjAyMyAwLDI3LjI1IDEuOTA1OTI4Myw3LjkzNzg1MiA2LjQ1NzU0MzIsMTMuNTkzNzQ4IDE0LjI0OTk5OTgsMTMuNTkzNzUgaCA5LjIxODc1IHYgLTEyLjI1IGMgMCwtOC44NDk5MDIgNy42NTcxNDQsLTE2LjY1NjI0OCAxNi43NSwtMTYuNjU2MjUgaCAyNi43ODEyNSBjIDcuNDU0OTUxLDAgMTMuNDA2MjUzLC02LjEzODE2NCAxMy40MDYyNSwtMTMuNjI1IHYgLTI1LjUzMTI1IGMgMCwtNy4yNjYzMzg2IC02LjEyOTk4LC0xMi43MjQ3NzcxIC0xMy40MDYyNSwtMTMuOTM3NDk5NyBDIDY0LjI4MTU0OCwwLjMyNzk0Mzk3IDU5LjUwMjQzOCwtMC4wMjAzNzkwMyA1NC45MTg3ODUsOS4xOTI3NDIxZS00IFogbSAtMTQuNSw4LjIxODc1MDEyNTc5IGMgMi43Njk1NDcsMCA1LjAzMTI1LDIuMjk4NjQ1NiA1LjAzMTI1LDUuMTI0OTk5NiAtMmUtNiwyLjgxNjMzNiAtMi4yNjE3MDMsNS4wOTM3NSAtNS4wMzEyNSw1LjA5Mzc1IC0yLjc3OTQ3NiwtMWUtNiAtNS4wMzEyNSwtMi4yNzc0MTUgLTUuMDMxMjUsLTUuMDkzNzUgLTEwZS03LC0yLjgyNjM1MyAyLjI1MTc3NCwtNS4xMjQ5OTk2IDUuMDMxMjUsLTUuMTI0OTk5NiB6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2ZmZDQzYiIgZD0ibSA4NS42Mzc1MzUsMjguNjU3MTY5IHYgMTEuOTA2MjUgYyAwLDkuMjMwNzU1IC03LjgyNTg5NSwxNi45OTk5OTkgLTE2Ljc1LDE3IGggLTI2Ljc4MTI1IGMgLTcuMzM1ODMzLDAgLTEzLjQwNjI0OSw2LjI3ODQ4MyAtMTMuNDA2MjUsMTMuNjI1IHYgMjUuNTMxMjQ3IGMgMCw3LjI2NjM0NCA2LjMxODU4OCwxMS41NDAzMjQgMTMuNDA2MjUsMTMuNjI1MDA0IDguNDg3MzMxLDIuNDk1NjEgMTYuNjI2MjM3LDIuOTQ2NjMgMjYuNzgxMjUsMCA2Ljc1MDE1NSwtMS45NTQzOSAxMy40MDYyNTMsLTUuODg3NjEgMTMuNDA2MjUsLTEzLjYyNTAwNCBWIDg2LjUwMDkxOSBoIC0yNi43ODEyNSB2IC0zLjQwNjI1IGggMjYuNzgxMjUgMTMuNDA2MjU0IGMgNy43OTI0NjEsMCAxMC42OTYyNTEsLTUuNDM1NDA4IDEzLjQwNjI0MSwtMTMuNTkzNzUgMi43OTkzMywtOC4zOTg4ODYgMi42ODAyMiwtMTYuNDc1Nzc2IDAsLTI3LjI1IC0xLjkyNTc4LC03Ljc1NzQ0MSAtNS42MDM4NywtMTMuNTkzNzUgLTEzLjQwNjI0MSwtMTMuNTkzNzUgeiBtIC0xNS4wNjI1LDY0LjY1NjI1IGMgMi43Nzk0NzgsM2UtNiA1LjAzMTI1LDIuMjc3NDE3IDUuMDMxMjUsNS4wOTM3NDcgLTJlLTYsMi44MjYzNTQgLTIuMjUxNzc1LDUuMTI1MDA0IC01LjAzMTI1LDUuMTI1MDA0IC0yLjc2OTU1LDAgLTUuMDMxMjUsLTIuMjk4NjUgLTUuMDMxMjUsLTUuMTI1MDA0IDJlLTYsLTIuODE2MzMgMi4yNjE2OTcsLTUuMDkzNzQ3IDUuMDMxMjUsLTUuMDkzNzQ3IHoiLz4KPC9zdmc+Cg==);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-redo: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PHBhdGggZD0iTTE4LjQgMTAuNkMxNi41NSA4Ljk5IDE0LjE1IDggMTEuNSA4Yy00LjY1IDAtOC41OCAzLjAzLTkuOTYgNy4yMkwzLjkgMTZjMS4wNS0zLjE5IDQuMDUtNS41IDcuNi01LjUgMS45NSAwIDMuNzMuNzIgNS4xMiAxLjg4TDEzIDE2aDlWN2wtMy42IDMuNnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-share: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTSAxOCAyIEMgMTYuMzU0OTkgMiAxNSAzLjM1NDk5MDQgMTUgNSBDIDE1IDUuMTkwOTUyOSAxNS4wMjE3OTEgNS4zNzcxMjI0IDE1LjA1NjY0MSA1LjU1ODU5MzggTCA3LjkyMTg3NSA5LjcyMDcwMzEgQyA3LjM5ODUzOTkgOS4yNzc4NTM5IDYuNzMyMDc3MSA5IDYgOSBDIDQuMzU0OTkwNCA5IDMgMTAuMzU0OTkgMyAxMiBDIDMgMTMuNjQ1MDEgNC4zNTQ5OTA0IDE1IDYgMTUgQyA2LjczMjA3NzEgMTUgNy4zOTg1Mzk5IDE0LjcyMjE0NiA3LjkyMTg3NSAxNC4yNzkyOTcgTCAxNS4wNTY2NDEgMTguNDM5NDUzIEMgMTUuMDIxNTU1IDE4LjYyMTUxNCAxNSAxOC44MDgzODYgMTUgMTkgQyAxNSAyMC42NDUwMSAxNi4zNTQ5OSAyMiAxOCAyMiBDIDE5LjY0NTAxIDIyIDIxIDIwLjY0NTAxIDIxIDE5IEMgMjEgMTcuMzU0OTkgMTkuNjQ1MDEgMTYgMTggMTYgQyAxNy4yNjc0OCAxNiAxNi42MDE1OTMgMTYuMjc5MzI4IDE2LjA3ODEyNSAxNi43MjI2NTYgTCA4Ljk0MzM1OTQgMTIuNTU4NTk0IEMgOC45NzgyMDk1IDEyLjM3NzEyMiA5IDEyLjE5MDk1MyA5IDEyIEMgOSAxMS44MDkwNDcgOC45NzgyMDk1IDExLjYyMjg3OCA4Ljk0MzM1OTQgMTEuNDQxNDA2IEwgMTYuMDc4MTI1IDcuMjc5Mjk2OSBDIDE2LjYwMTQ2IDcuNzIyMTQ2MSAxNy4yNjc5MjMgOCAxOCA4IEMgMTkuNjQ1MDEgOCAyMSA2LjY0NTAwOTYgMjEgNSBDIDIxIDMuMzU0OTkwNCAxOS42NDUwMSAyIDE4IDIgeiBNIDE4IDQgQyAxOC41NjQxMjkgNCAxOSA0LjQzNTg3MDYgMTkgNSBDIDE5IDUuNTY0MTI5NCAxOC41NjQxMjkgNiAxOCA2IEMgMTcuNDM1ODcxIDYgMTcgNS41NjQxMjk0IDE3IDUgQyAxNyA0LjQzNTg3MDYgMTcuNDM1ODcxIDQgMTggNCB6IE0gNiAxMSBDIDYuNTY0MTI5NCAxMSA3IDExLjQzNTg3MSA3IDEyIEMgNyAxMi41NjQxMjkgNi41NjQxMjk0IDEzIDYgMTMgQyA1LjQzNTg3MDYgMTMgNSAxMi41NjQxMjkgNSAxMiBDIDUgMTEuNDM1ODcxIDUuNDM1ODcwNiAxMSA2IDExIHogTSAxOCAxOCBDIDE4LjU2NDEyOSAxOCAxOSAxOC40MzU4NzEgMTkgMTkgQyAxOSAxOS41NjQxMjkgMTguNTY0MTI5IDIwIDE4IDIwIEMgMTcuNDM1ODcxIDIwIDE3IDE5LjU2NDEyOSAxNyAxOSBDIDE3IDE4LjQzNTg3MSAxNy40MzU4NzEgMTggMTggMTggeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-table-rows: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMSw4SDNWNGgxOFY4eiBNMjEsMTBIM3Y0aDE4VjEweiBNMjEsMTZIM3Y0aDE4VjE2eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-tag: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjgiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCA0MyAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTI4LjgzMzIgMTIuMzM0TDMyLjk5OTggMTYuNTAwN0wzNy4xNjY1IDEyLjMzNEgyOC44MzMyWiIvPgoJCTxwYXRoIGQ9Ik0xNi4yMDk1IDIxLjYxMDRDMTUuNjg3MyAyMi4xMjk5IDE0Ljg0NDMgMjIuMTI5OSAxNC4zMjQ4IDIxLjYxMDRMNi45ODI5IDE0LjcyNDVDNi41NzI0IDE0LjMzOTQgNi4wODMxMyAxMy42MDk4IDYuMDQ3ODYgMTMuMDQ4MkM1Ljk1MzQ3IDExLjUyODggNi4wMjAwMiA4LjYxOTQ0IDYuMDY2MjEgNy4wNzY5NUM2LjA4MjgxIDYuNTE0NzcgNi41NTU0OCA2LjA0MzQ3IDcuMTE4MDQgNi4wMzA1NUM5LjA4ODYzIDUuOTg0NzMgMTMuMjYzOCA1LjkzNTc5IDEzLjY1MTggNi4zMjQyNUwyMS43MzY5IDEzLjYzOUMyMi4yNTYgMTQuMTU4NSAyMS43ODUxIDE1LjQ3MjQgMjEuMjYyIDE1Ljk5NDZMMTYuMjA5NSAyMS42MTA0Wk05Ljc3NTg1IDguMjY1QzkuMzM1NTEgNy44MjU2NiA4LjYyMzUxIDcuODI1NjYgOC4xODI4IDguMjY1QzcuNzQzNDYgOC43MDU3MSA3Ljc0MzQ2IDkuNDE3MzMgOC4xODI4IDkuODU2NjdDOC42MjM4MiAxMC4yOTY0IDkuMzM1ODIgMTAuMjk2NCA5Ljc3NTg1IDkuODU2NjdDMTAuMjE1NiA5LjQxNzMzIDEwLjIxNTYgOC43MDUzMyA5Ljc3NTg1IDguMjY1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtdGVybWluYWwtaWNvbi1iYWNrZ3JvdW5kLWNvbG9yIGpwLWljb24tc2VsZWN0YWJsZSIgd2lkdGg9IjIwIiBoZWlnaHQ9IjIwIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgyIDIpIiBmaWxsPSIjMzMzMzMzIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtdGVybWluYWwtaWNvbi1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUtaW52ZXJzZSIgZD0iTTUuMDU2NjQgOC43NjE3MkM1LjA1NjY0IDguNTk3NjYgNS4wMzEyNSA4LjQ1MzEyIDQuOTgwNDcgOC4zMjgxMkM0LjkzMzU5IDguMTk5MjIgNC44NTU0NyA4LjA4MjAzIDQuNzQ2MDkgNy45NzY1NkM0LjY0MDYyIDcuODcxMDkgNC41IDcuNzc1MzkgNC4zMjQyMiA3LjY4OTQ1QzQuMTUyMzQgNy41OTk2MSAzLjk0MzM2IDcuNTExNzIgMy42OTcyNyA3LjQyNTc4QzMuMzAyNzMgNy4yODUxNiAyLjk0MzM2IDcuMTM2NzIgMi42MTkxNCA2Ljk4MDQ3QzIuMjk0OTIgNi44MjQyMiAyLjAxNzU4IDYuNjQyNTggMS43ODcxMSA2LjQzNTU1QzEuNTYwNTUgNi4yMjg1MiAxLjM4NDc3IDUuOTg4MjggMS4yNTk3NyA1LjcxNDg0QzEuMTM0NzcgNS40Mzc1IDEuMDcyMjcgNS4xMDkzOCAxLjA3MjI3IDQuNzMwNDdDMS4wNzIyNyA0LjM5ODQ0IDEuMTI4OTEgNC4wOTU3IDEuMjQyMTkgMy44MjIyN0MxLjM1NTQ3IDMuNTQ0OTIgMS41MTU2MiAzLjMwNDY5IDEuNzIyNjYgMy4xMDE1NkMxLjkyOTY5IDIuODk4NDQgMi4xNzk2OSAyLjczNDM3IDIuNDcyNjYgMi42MDkzOEMyLjc2NTYyIDIuNDg0MzggMy4wOTE4IDIuNDA0MyAzLjQ1MTE3IDIuMzY5MTRWMS4xMDkzOEg0LjM4ODY3VjIuMzgwODZDNC43NDAyMyAyLjQyNzczIDUuMDU2NjQgMi41MjM0NCA1LjMzNzg5IDIuNjY3OTdDNS42MTkxNCAyLjgxMjUgNS44NTc0MiAzLjAwMTk1IDYuMDUyNzMgMy4yMzYzM0M2LjI1MTk1IDMuNDY2OCA2LjQwNDMgMy43NDAyMyA2LjUwOTc3IDQuMDU2NjRDNi42MTkxNCA0LjM2OTE0IDYuNjczODMgNC43MjA3IDYuNjczODMgNS4xMTEzM0g1LjA0NDkyQzUuMDQ0OTIgNC42Mzg2NyA0LjkzNzUgNC4yODEyNSA0LjcyMjY2IDQuMDM5MDZDNC41MDc4MSAzLjc5Mjk3IDQuMjE2OCAzLjY2OTkyIDMuODQ5NjEgMy42Njk5MkMzLjY1MDM5IDMuNjY5OTIgMy40NzY1NiAzLjY5NzI3IDMuMzI4MTIgMy43NTE5NUMzLjE4MzU5IDMuODAyNzMgMy4wNjQ0NSAzLjg3Njk1IDIuOTcwNyAzLjk3NDYxQzIuODc2OTUgNC4wNjgzNiAyLjgwNjY0IDQuMTc5NjkgMi43NTk3NyA0LjMwODU5QzIuNzE2OCA0LjQzNzUgMi42OTUzMSA0LjU3ODEyIDIuNjk1MzEgNC43MzA0N0MyLjY5NTMxIDQuODgyODEgMi43MTY4IDUuMDE5NTMgMi43NTk3NyA1LjE0MDYyQzIuODA2NjQgNS4yNTc4MSAyLjg4MjgxIDUuMzY3MTkgMi45ODgyOCA1LjQ2ODc1QzMuMDk3NjYgNS41NzAzMSAzLjI0MDIzIDUuNjY3OTcgMy40MTYwMiA1Ljc2MTcyQzMuNTkxOCA1Ljg1MTU2IDMuODEwNTUgNS45NDMzNiA0LjA3MjI3IDYuMDM3MTFDNC40NjY4IDYuMTg1NTUgNC44MjQyMiA2LjMzOTg0IDUuMTQ0NTMgNi41QzUuNDY0ODQgNi42NTYyNSA1LjczODI4IDYuODM5ODQgNS45NjQ4NCA3LjA1MDc4QzYuMTk1MzEgNy4yNTc4MSA2LjM3MTA5IDcuNSA2LjQ5MjE5IDcuNzc3MzRDNi42MTcxOSA4LjA1MDc4IDYuNjc5NjkgOC4zNzUgNi42Nzk2OSA4Ljc1QzYuNjc5NjkgOS4wOTM3NSA2LjYyMzA1IDkuNDA0MyA2LjUwOTc3IDkuNjgxNjRDNi4zOTY0OCA5Ljk1NTA4IDYuMjM0MzggMTAuMTkxNCA2LjAyMzQ0IDEwLjM5MDZDNS44MTI1IDEwLjU4OTggNS41NTg1OSAxMC43NSA1LjI2MTcyIDEwLjg3MTFDNC45NjQ4NCAxMC45ODgzIDQuNjMyODEgMTEuMDY0NSA0LjI2NTYyIDExLjA5OTZWMTIuMjQ4SDMuMzMzOThWMTEuMDk5NkMzLjAwMTk1IDExLjA2ODQgMi42Nzk2OSAxMC45OTYxIDIuMzY3MTkgMTAuODgyOEMyLjA1NDY5IDEwLjc2NTYgMS43NzczNCAxMC41OTc3IDEuNTM1MTYgMTAuMzc4OUMxLjI5Njg4IDEwLjE2MDIgMS4xMDU0NyA5Ljg4NDc3IDAuOTYwOTM4IDkuNTUyNzNDMC44MTY0MDYgOS4yMTY4IDAuNzQ0MTQxIDguODE0NDUgMC43NDQxNDEgOC4zNDU3SDIuMzc4OTFDMi4zNzg5MSA4LjYyNjk1IDIuNDE5OTIgOC44NjMyOCAyLjUwMTk1IDkuMDU0NjlDMi41ODM5OCA5LjI0MjE5IDIuNjg5NDUgOS4zOTI1OCAyLjgxODM2IDkuNTA1ODZDMi45NTExNyA5LjYxNTIzIDMuMTAxNTYgOS42OTMzNiAzLjI2OTUzIDkuNzQwMjNDMy40Mzc1IDkuNzg3MTEgMy42MDkzOCA5LjgxMDU1IDMuNzg1MTYgOS44MTA1NUM0LjIwMzEyIDkuODEwNTUgNC41MTk1MyA5LjcxMjg5IDQuNzM0MzggOS41MTc1OEM0Ljk0OTIyIDkuMzIyMjcgNS4wNTY2NCA5LjA3MDMxIDUuMDU2NjQgOC43NjE3MlpNMTMuNDE4IDEyLjI3MTVIOC4wNzQyMlYxMUgxMy40MThWMTIuMjcxNVoiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMuOTUyNjQgNikiIGZpbGw9IndoaXRlIi8+Cjwvc3ZnPgo=);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtdGV4dC1lZGl0b3ItaWNvbi1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xNSAxNUgzdjJoMTJ2LTJ6bTAtOEgzdjJoMTJWN3pNMyAxM2gxOHYtMkgzdjJ6bTAgOGgxOHYtMkgzdjJ6TTMgM3YyaDE4VjNIM3oiLz4KPC9zdmc+Cg==);
  --jp-icon-toc: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik03LDVIMjFWN0g3VjVNNywxM1YxMUgyMVYxM0g3TTQsNC41QTEuNSwxLjUgMCAwLDEgNS41LDZBMS41LDEuNSAwIDAsMSA0LDcuNUExLjUsMS41IDAgMCwxIDIuNSw2QTEuNSwxLjUgMCAwLDEgNCw0LjVNNCwxMC41QTEuNSwxLjUgMCAwLDEgNS41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMy41QTEuNSwxLjUgMCAwLDEgMi41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMC41TTcsMTlWMTdIMjFWMTlIN000LDE2LjVBMS41LDEuNSAwIDAsMSA1LjUsMThBMS41LDEuNSAwIDAsMSA0LDE5LjVBMS41LDEuNSAwIDAsMSAyLjUsMThBMS41LDEuNSAwIDAsMSA0LDE2LjVaIiAvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tree-view: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMiAxMVYzaC03djNIOVYzSDJ2OGg3VjhoMnYxMGg0djNoN3YtOGgtN3YzaC0yVjhoMnYzeiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-user: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE2IDdhNCA0IDAgMTEtOCAwIDQgNCAwIDAxOCAwek0xMiAxNGE3IDcgMCAwMC03IDdoMTRhNyA3IDAgMDAtNy03eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-users: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZlcnNpb249IjEuMSIgdmlld0JveD0iMCAwIDM2IDI0IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPgogPGcgY2xhc3M9ImpwLWljb24zIiB0cmFuc2Zvcm09Im1hdHJpeCgxLjczMjcgMCAwIDEuNzMyNyAtMy42MjgyIC4wOTk1NzcpIiBmaWxsPSIjNjE2MTYxIj4KICA8cGF0aCB0cmFuc2Zvcm09Im1hdHJpeCgxLjUsMCwwLDEuNSwwLC02KSIgZD0ibTEyLjE4NiA3LjUwOThjLTEuMDUzNSAwLTEuOTc1NyAwLjU2NjUtMi40Nzg1IDEuNDEwMiAwLjc1MDYxIDAuMzEyNzcgMS4zOTc0IDAuODI2NDggMS44NzMgMS40NzI3aDMuNDg2M2MwLTEuNTkyLTEuMjg4OS0yLjg4MjgtMi44ODA5LTIuODgyOHoiLz4KICA8cGF0aCBkPSJtMjAuNDY1IDIuMzg5NWEyLjE4ODUgMi4xODg1IDAgMCAxLTIuMTg4NCAyLjE4ODUgMi4xODg1IDIuMTg4NSAwIDAgMS0yLjE4ODUtMi4xODg1IDIuMTg4NSAyLjE4ODUgMCAwIDEgMi4xODg1LTIuMTg4NSAyLjE4ODUgMi4xODg1IDAgMCAxIDIuMTg4NCAyLjE4ODV6Ii8+CiAgPHBhdGggdHJhbnNmb3JtPSJtYXRyaXgoMS41LDAsMCwxLjUsMCwtNikiIGQ9Im0zLjU4OTggOC40MjE5Yy0xLjExMjYgMC0yLjAxMzcgMC45MDExMS0yLjAxMzcgMi4wMTM3aDIuODE0NWMwLjI2Nzk3LTAuMzczMDkgMC41OTA3LTAuNzA0MzUgMC45NTg5OC0wLjk3ODUyLTAuMzQ0MzMtMC42MTY4OC0xLjAwMzEtMS4wMzUyLTEuNzU5OC0xLjAzNTJ6Ii8+CiAgPHBhdGggZD0ibTYuOTE1NCA0LjYyM2ExLjUyOTQgMS41Mjk0IDAgMCAxLTEuNTI5NCAxLjUyOTQgMS41Mjk0IDEuNTI5NCAwIDAgMS0xLjUyOTQtMS41Mjk0IDEuNTI5NCAxLjUyOTQgMCAwIDEgMS41Mjk0LTEuNTI5NCAxLjUyOTQgMS41Mjk0IDAgMCAxIDEuNTI5NCAxLjUyOTR6Ii8+CiAgPHBhdGggZD0ibTYuMTM1IDEzLjUzNWMwLTMuMjM5MiAyLjYyNTktNS44NjUgNS44NjUtNS44NjUgMy4yMzkyIDAgNS44NjUgMi42MjU5IDUuODY1IDUuODY1eiIvPgogIDxjaXJjbGUgY3g9IjEyIiBjeT0iMy43Njg1IiByPSIyLjk2ODUiLz4KIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-word: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KIDxnIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzQxNDE0MSI+CiAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiA8L2c+CiA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSguNDMgLjA0MDEpIiBmaWxsPSIjZmZmIj4KICA8cGF0aCBkPSJtNC4xNCA4Ljc2cTAuMDY4Mi0xLjg5IDIuNDItMS44OSAxLjE2IDAgMS42OCAwLjQyIDAuNTY3IDAuNDEgMC41NjcgMS4xNnYzLjQ3cTAgMC40NjIgMC41MTQgMC40NjIgMC4xMDMgMCAwLjItMC4wMjMxdjAuNzE0cS0wLjM5OSAwLjEwMy0wLjY1MSAwLjEwMy0wLjQ1MiAwLTAuNjkzLTAuMjItMC4yMzEtMC4yLTAuMjg0LTAuNjYyLTAuOTU2IDAuODcyLTIgMC44NzItMC45MDMgMC0xLjQ3LTAuNDcyLTAuNTI1LTAuNDcyLTAuNTI1LTEuMjYgMC0wLjI2MiAwLjA0NTItMC40NzIgMC4wNTY3LTAuMjIgMC4xMTYtMC4zNzggMC4wNjgyLTAuMTY4IDAuMjMxLTAuMzA0IDAuMTU4LTAuMTQ3IDAuMjYyLTAuMjQyIDAuMTE2LTAuMDkxNCAwLjM2OC0wLjE2OCAwLjI2Mi0wLjA5MTQgMC4zOTktMC4xMjYgMC4xMzYtMC4wNDUyIDAuNDcyLTAuMTAzIDAuMzM2LTAuMDU3OCAwLjUwNC0wLjA3OTggMC4xNTgtMC4wMjMxIDAuNTY3LTAuMDc5OCAwLjU1Ni0wLjA2ODIgMC43NzctMC4yMjEgMC4yMi0wLjE1MiAwLjIyLTAuNDQxdi0wLjI1MnEwLTAuNDMtMC4zNTctMC42NjItMC4zMzYtMC4yMzEtMC45NzYtMC4yMzEtMC42NjIgMC0wLjk5OCAwLjI2Mi0wLjMzNiAwLjI1Mi0wLjM5OSAwLjc5OHptMS44OSAzLjY4cTAuNzg4IDAgMS4yNi0wLjQxIDAuNTA0LTAuNDIgMC41MDQtMC45MDN2LTEuMDVxLTAuMjg0IDAuMTM2LTAuODYxIDAuMjMxLTAuNTY3IDAuMDkxNC0wLjk4NyAwLjE1OC0wLjQyIDAuMDY4Mi0wLjc2NiAwLjMyNi0wLjMzNiAwLjI1Mi0wLjMzNiAwLjcwNHQwLjMwNCAwLjcwNCAwLjg2MSAwLjI1MnoiIHN0cm9rZS13aWR0aD0iMS4wNSIvPgogIDxwYXRoIGQ9Im0xMCA0LjU2aDAuOTQ1djMuMTVxMC42NTEtMC45NzYgMS44OS0wLjk3NiAxLjE2IDAgMS44OSAwLjg0IDAuNjgyIDAuODQgMC42ODIgMi4zMSAwIDEuNDctMC43MDQgMi40Mi0wLjcwNCAwLjg4Mi0xLjg5IDAuODgyLTEuMjYgMC0xLjg5LTEuMDJ2MC43NjZoLTAuODV6bTIuNjIgMy4wNHEtMC43NDYgMC0xLjE2IDAuNjQtMC40NTIgMC42My0wLjQ1MiAxLjY4IDAgMS4wNSAwLjQ1MiAxLjY4dDEuMTYgMC42M3EwLjc3NyAwIDEuMjYtMC42MyAwLjQ5NC0wLjY0IDAuNDk0LTEuNjggMC0xLjA1LTAuNDcyLTEuNjgtMC40NjItMC42NC0xLjI2LTAuNjR6IiBzdHJva2Utd2lkdGg9IjEuMDUiLz4KICA8cGF0aCBkPSJtMi43MyAxNS44IDEzLjYgMC4wMDgxYzAuMDA2OSAwIDAtMi42IDAtMi42IDAtMC4wMDc4LTEuMTUgMC0xLjE1IDAtMC4wMDY5IDAtMC4wMDgzIDEuNS0wLjAwODMgMS41LTJlLTMgLTAuMDAxNC0xMS4zLTAuMDAxNC0xMS4zLTAuMDAxNGwtMC4wMDU5Mi0xLjVjMC0wLjAwNzgtMS4xNyAwLjAwMTMtMS4xNyAwLjAwMTN6IiBzdHJva2Utd2lkdGg9Ii45NzUiLz4KIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddAboveIcon {
  background-image: var(--jp-icon-add-above);
}

.jp-AddBelowIcon {
  background-image: var(--jp-icon-add-below);
}

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}

.jp-BellIcon {
  background-image: var(--jp-icon-bell);
}

.jp-BugDotIcon {
  background-image: var(--jp-icon-bug-dot);
}

.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}

.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}

.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}

.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}

.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}

.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}

.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}

.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}

.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}

.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}

.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}

.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}

.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}

.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}

.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}

.jp-CodeCheckIcon {
  background-image: var(--jp-icon-code-check);
}

.jp-CodeIcon {
  background-image: var(--jp-icon-code);
}

.jp-CollapseAllIcon {
  background-image: var(--jp-icon-collapse-all);
}

.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}

.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}

.jp-CopyrightIcon {
  background-image: var(--jp-icon-copyright);
}

.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}

.jp-DeleteIcon {
  background-image: var(--jp-icon-delete);
}

.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}

.jp-DuplicateIcon {
  background-image: var(--jp-icon-duplicate);
}

.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}

.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}

.jp-ErrorIcon {
  background-image: var(--jp-icon-error);
}

.jp-ExpandAllIcon {
  background-image: var(--jp-icon-expand-all);
}

.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}

.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}

.jp-FileIcon {
  background-image: var(--jp-icon-file);
}

.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}

.jp-FilterDotIcon {
  background-image: var(--jp-icon-filter-dot);
}

.jp-FilterIcon {
  background-image: var(--jp-icon-filter);
}

.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}

.jp-FolderFavoriteIcon {
  background-image: var(--jp-icon-folder-favorite);
}

.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}

.jp-HomeIcon {
  background-image: var(--jp-icon-home);
}

.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}

.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}

.jp-InfoIcon {
  background-image: var(--jp-icon-info);
}

.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}

.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}

.jp-JuliaIcon {
  background-image: var(--jp-icon-julia);
}

.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}

.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}

.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}

.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}

.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}

.jp-LaunchIcon {
  background-image: var(--jp-icon-launch);
}

.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}

.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}

.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}

.jp-ListIcon {
  background-image: var(--jp-icon-list);
}

.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}

.jp-MoveDownIcon {
  background-image: var(--jp-icon-move-down);
}

.jp-MoveUpIcon {
  background-image: var(--jp-icon-move-up);
}

.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}

.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}

.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}

.jp-NumberingIcon {
  background-image: var(--jp-icon-numbering);
}

.jp-OfflineBoltIcon {
  background-image: var(--jp-icon-offline-bolt);
}

.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}

.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}

.jp-PdfIcon {
  background-image: var(--jp-icon-pdf);
}

.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}

.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}

.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}

.jp-RedoIcon {
  background-image: var(--jp-icon-redo);
}

.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}

.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}

.jp-RunIcon {
  background-image: var(--jp-icon-run);
}

.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}

.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}

.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}

.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}

.jp-ShareIcon {
  background-image: var(--jp-icon-share);
}

.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}

.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}

.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}

.jp-TableRowsIcon {
  background-image: var(--jp-icon-table-rows);
}

.jp-TagIcon {
  background-image: var(--jp-icon-tag);
}

.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}

.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}

.jp-TocIcon {
  background-image: var(--jp-icon-toc);
}

.jp-TreeViewIcon {
  background-image: var(--jp-icon-tree-view);
}

.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}

.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}

.jp-UserIcon {
  background-image: var(--jp-icon-user);
}

.jp-UsersIcon {
  background-image: var(--jp-icon-users);
}

.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}

.jp-WordIcon {
  background-image: var(--jp-icon-word);
}

.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.lm-TabBar .lm-TabBar-addButton {
  align-items: center;
  display: flex;
  padding: 4px;
  padding-bottom: 5px;
  margin-right: 1px;
  background-color: var(--jp-layout-color2);
}

.lm-TabBar .lm-TabBar-addButton:hover {
  background-color: var(--jp-layout-color1);
}

.lm-DockPanel-tabBar .lm-TabBar-tab {
  width: var(--jp-private-horizontal-tab-width);
}

.lm-DockPanel-tabBar .lm-TabBar-content {
  flex: unset;
}

.lm-DockPanel-tabBar[data-orientation='horizontal'] {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}

/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}

.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}

.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}

.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}

.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}

.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}

.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}

.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}

.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}

/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}

.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}

.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}

.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}

.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}

.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}

.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}

/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}

.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}

.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}

.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}

.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}

.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}

.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

.jp-icon-dot[fill] {
  fill: var(--jp-warn-color0);
}

.jp-jupyter-icon-color[fill] {
  fill: var(--jp-jupyter-icon-color, var(--jp-warn-color0));
}

.jp-notebook-icon-color[fill] {
  fill: var(--jp-notebook-icon-color, var(--jp-warn-color0));
}

.jp-json-icon-color[fill] {
  fill: var(--jp-json-icon-color, var(--jp-warn-color1));
}

.jp-console-icon-color[fill] {
  fill: var(--jp-console-icon-color, white);
}

.jp-console-icon-background-color[fill] {
  fill: var(--jp-console-icon-background-color, var(--jp-brand-color1));
}

.jp-terminal-icon-color[fill] {
  fill: var(--jp-terminal-icon-color, var(--jp-layout-color2));
}

.jp-terminal-icon-background-color[fill] {
  fill: var(
    --jp-terminal-icon-background-color,
    var(--jp-inverse-layout-color2)
  );
}

.jp-text-editor-icon-color[fill] {
  fill: var(--jp-text-editor-icon-color, var(--jp-inverse-layout-color3));
}

.jp-inspector-icon-color[fill] {
  fill: var(--jp-inspector-icon-color, var(--jp-inverse-layout-color3));
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* stylelint-disable selector-max-class, selector-max-compound-selectors */

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}

.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* stylelint-enable selector-max-class, selector-max-compound-selectors */

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) .jp-icon-hoverShow-content {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `lm-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FormGroup-content fieldset {
  border: none;
  padding: 0;
  min-width: 0;
  width: 100%;
}

/* stylelint-disable selector-max-type */

.jp-FormGroup-content fieldset .jp-inputFieldWrapper input,
.jp-FormGroup-content fieldset .jp-inputFieldWrapper select,
.jp-FormGroup-content fieldset .jp-inputFieldWrapper textarea {
  font-size: var(--jp-content-font-size2);
  border-color: var(--jp-input-border-color);
  border-style: solid;
  border-radius: var(--jp-border-radius);
  border-width: 1px;
  padding: 6px 8px;
  background: none;
  color: var(--jp-ui-font-color0);
  height: inherit;
}

.jp-FormGroup-content fieldset input[type='checkbox'] {
  position: relative;
  top: 2px;
  margin-left: 0;
}

.jp-FormGroup-content button.jp-mod-styled {
  cursor: pointer;
}

.jp-FormGroup-content .checkbox label {
  cursor: pointer;
  font-size: var(--jp-content-font-size1);
}

.jp-FormGroup-content .jp-root > fieldset > legend {
  display: none;
}

.jp-FormGroup-content .jp-root > fieldset > p {
  display: none;
}

/** copy of `input.jp-mod-styled:focus` style */
.jp-FormGroup-content fieldset input:focus,
.jp-FormGroup-content fieldset select:focus {
  -moz-outline-radius: unset;
  outline: var(--jp-border-width) solid var(--md-blue-500);
  outline-offset: -1px;
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-FormGroup-content fieldset input:hover:not(:focus),
.jp-FormGroup-content fieldset select:hover:not(:focus) {
  background-color: var(--jp-border-color2);
}

/* stylelint-enable selector-max-type */

.jp-FormGroup-content .checkbox .field-description {
  /* Disable default description field for checkbox:
   because other widgets do not have description fields,
   we add descriptions to each widget on the field level.
  */
  display: none;
}

.jp-FormGroup-content #root__description {
  display: none;
}

.jp-FormGroup-content .jp-modifiedIndicator {
  width: 5px;
  background-color: var(--jp-brand-color2);
  margin-top: 0;
  margin-left: calc(var(--jp-private-settingeditor-modifier-indent) * -1);
  flex-shrink: 0;
}

.jp-FormGroup-content .jp-modifiedIndicator.jp-errorIndicator {
  background-color: var(--jp-error-color0);
  margin-right: 0.5em;
}

/* RJSF ARRAY style */

.jp-arrayFieldWrapper legend {
  font-size: var(--jp-content-font-size2);
  color: var(--jp-ui-font-color0);
  flex-basis: 100%;
  padding: 4px 0;
  font-weight: var(--jp-content-heading-font-weight);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-arrayFieldWrapper .field-description {
  padding: 4px 0;
  white-space: pre-wrap;
}

.jp-arrayFieldWrapper .array-item {
  width: 100%;
  border: 1px solid var(--jp-border-color2);
  border-radius: 4px;
  margin: 4px;
}

.jp-ArrayOperations {
  display: flex;
  margin-left: 8px;
}

.jp-ArrayOperationsButton {
  margin: 2px;
}

.jp-ArrayOperationsButton .jp-icon3[fill] {
  fill: var(--jp-ui-font-color0);
}

button.jp-ArrayOperationsButton.jp-mod-styled:disabled {
  cursor: not-allowed;
  opacity: 0.5;
}

/* RJSF form validation error */

.jp-FormGroup-content .validationErrors {
  color: var(--jp-error-color0);
}

/* Hide panel level error as duplicated the field level error */
.jp-FormGroup-content .panel.errors {
  display: none;
}

/* RJSF normal content (settings-editor) */

.jp-FormGroup-contentNormal {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.jp-FormGroup-contentNormal .jp-FormGroup-contentItem {
  margin-left: 7px;
  color: var(--jp-ui-font-color0);
}

.jp-FormGroup-contentNormal .jp-FormGroup-description {
  flex-basis: 100%;
  padding: 4px 7px;
}

.jp-FormGroup-contentNormal .jp-FormGroup-default {
  flex-basis: 100%;
  padding: 4px 7px;
}

.jp-FormGroup-contentNormal .jp-FormGroup-fieldLabel {
  font-size: var(--jp-content-font-size1);
  font-weight: normal;
  min-width: 120px;
}

.jp-FormGroup-contentNormal fieldset:not(:first-child) {
  margin-left: 7px;
}

.jp-FormGroup-contentNormal .field-array-of-string .array-item {
  /* Display `jp-ArrayOperations` buttons side-by-side with content except
    for small screens where flex-wrap will place them one below the other.
  */
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.jp-FormGroup-contentNormal .jp-objectFieldWrapper .form-group {
  padding: 2px 8px 2px var(--jp-private-settingeditor-modifier-indent);
  margin-top: 2px;
}

/* RJSF compact content (metadata-form) */

.jp-FormGroup-content.jp-FormGroup-contentCompact {
  width: 100%;
}

.jp-FormGroup-contentCompact .form-group {
  display: flex;
  padding: 0.5em 0.2em 0.5em 0;
}

.jp-FormGroup-contentCompact
  .jp-FormGroup-compactTitle
  .jp-FormGroup-description {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color2);
}

.jp-FormGroup-contentCompact .jp-FormGroup-fieldLabel {
  padding-bottom: 0.3em;
}

.jp-FormGroup-contentCompact .jp-inputFieldWrapper .form-control {
  width: 100%;
  box-sizing: border-box;
}

.jp-FormGroup-contentCompact .jp-arrayFieldWrapper .jp-FormGroup-compactTitle {
  padding-bottom: 7px;
}

.jp-FormGroup-contentCompact
  .jp-objectFieldWrapper
  .jp-objectFieldWrapper
  .form-group {
  padding: 2px 8px 2px var(--jp-private-settingeditor-modifier-indent);
  margin-top: 2px;
}

.jp-FormGroup-contentCompact ul.error-detail {
  margin-block-start: 0.5em;
  margin-block-end: 0.5em;
  padding-inline-start: 1em;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-SidePanel {
  display: flex;
  flex-direction: column;
  min-width: var(--jp-sidebar-min-width);
  overflow-y: auto;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size1);
}

.jp-SidePanel-header {
  flex: 0 0 auto;
  display: flex;
  border-bottom: var(--jp-border-width) solid var(--jp-border-color2);
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin: 0;
  padding: 2px;
  text-transform: uppercase;
}

.jp-SidePanel-toolbar {
  flex: 0 0 auto;
}

.jp-SidePanel-content {
  flex: 1 1 auto;
}

.jp-SidePanel-toolbar,
.jp-AccordionPanel-toolbar {
  height: var(--jp-private-toolbar-height);
}

.jp-SidePanel-toolbar.jp-Toolbar-micro {
  display: none;
}

.lm-AccordionPanel .jp-AccordionPanel-title {
  box-sizing: border-box;
  line-height: 25px;
  margin: 0;
  display: flex;
  align-items: center;
  background: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  font-size: var(--jp-ui-font-size0);
}

.jp-AccordionPanel-title {
  cursor: pointer;
  user-select: none;
  -moz-user-select: none;
  -webkit-user-select: none;
  text-transform: uppercase;
}

.lm-AccordionPanel[data-orientation='horizontal'] > .jp-AccordionPanel-title {
  /* Title is rotated for horizontal accordion panel using CSS */
  display: block;
  transform-origin: top left;
  transform: rotate(-90deg) translate(-100%);
}

.jp-AccordionPanel-title .lm-AccordionPanel-titleLabel {
  user-select: none;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}

.jp-AccordionPanel-title .lm-AccordionPanel-titleCollapser {
  transform: rotate(-90deg);
  margin: auto 0;
  height: 16px;
}

.jp-AccordionPanel-title.lm-mod-expanded .lm-AccordionPanel-titleCollapser {
  transform: rotate(0deg);
}

.lm-AccordionPanel .jp-AccordionPanel-toolbar {
  background: none;
  box-shadow: none;
  border: none;
  margin-left: auto;
}

.lm-AccordionPanel .lm-SplitPanel-handle:hover {
  background: var(--jp-layout-color3);
}

.jp-text-truncated {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent::before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent::after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input[type='checkbox'].jp-mod-styled {
  appearance: checkbox;
  -webkit-appearance: checkbox;
  -moz-appearance: checkbox;
  height: auto;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper:not(.multiple) {
  height: 28px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

select.jp-mod-styled:not([multiple]) {
  height: 32px;
}

select.jp-mod-styled[multiple] {
  max-height: 200px;
  overflow-y: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-switch {
  display: flex;
  align-items: center;
  padding-left: 4px;
  padding-right: 4px;
  font-size: var(--jp-ui-font-size1);
  background-color: transparent;
  color: var(--jp-ui-font-color1);
  border: none;
  height: 20px;
}

.jp-switch:hover {
  background-color: var(--jp-layout-color2);
}

.jp-switch-label {
  margin-right: 5px;
  font-family: var(--jp-ui-font-family);
}

.jp-switch-track {
  cursor: pointer;
  background-color: var(--jp-switch-color, var(--jp-border-color1));
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 34px;
  height: 16px;
  width: 35px;
  position: relative;
}

.jp-switch-track::before {
  content: '';
  position: absolute;
  height: 10px;
  width: 10px;
  margin: 3px;
  left: 0;
  background-color: var(--jp-ui-inverse-font-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 50%;
}

.jp-switch[aria-checked='true'] .jp-switch-track {
  background-color: var(--jp-switch-true-position-color, var(--jp-warn-color0));
}

.jp-switch[aria-checked='true'] .jp-switch-track::before {
  /* track width (35) - margins (3 + 3) - thumb width (10) */
  left: 19px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 8;
  overflow-x: hidden;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0;
  margin: 0;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0 6px;
  margin: 0;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent > span {
  padding: 0;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
  font-family: var(--jp-ui-font-family);
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar.jp-Toolbar-micro {
  padding: 0;
  min-height: 0;
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar {
  border: none;
  box-shadow: none;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-WindowedPanel-outer {
  position: relative;
  overflow-y: auto;
}

.jp-WindowedPanel-inner {
  position: relative;
}

.jp-WindowedPanel-window {
  position: absolute;
  left: 0;
  right: 0;
  overflow: visible;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

body {
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
}

/* Disable native link decoration styles everywhere outside of dialog boxes */
a {
  text-decoration: unset;
  color: unset;
}

a:hover {
  text-decoration: unset;
  color: unset;
}

/* Accessibility for links inside dialog box text */
.jp-Dialog-content a {
  text-decoration: revert;
  color: var(--jp-content-link-color);
}

.jp-Dialog-content a:hover {
  text-decoration: revert;
}

/* Styles for ui-components */
.jp-Button {
  color: var(--jp-ui-font-color2);
  border-radius: var(--jp-border-radius);
  padding: 0 12px;
  font-size: var(--jp-ui-font-size1);

  /* Copy from blueprint 3 */
  display: inline-flex;
  flex-direction: row;
  border: none;
  cursor: pointer;
  align-items: center;
  justify-content: center;
  text-align: left;
  vertical-align: middle;
  min-height: 30px;
  min-width: 30px;
}

.jp-Button:disabled {
  cursor: not-allowed;
}

.jp-Button:empty {
  padding: 0 !important;
}

.jp-Button.jp-mod-small {
  min-height: 24px;
  min-width: 24px;
  font-size: 12px;
  padding: 0 7px;
}

/* Use our own theme for hover styles */
.jp-Button.jp-mod-minimal:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Button.jp-mod-minimal {
  background: none;
}

.jp-InputGroup {
  display: block;
  position: relative;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border: none;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
  padding-bottom: 0;
  padding-top: 0;
  padding-left: 10px;
  padding-right: 28px;
  position: relative;
  width: 100%;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  font-size: 14px;
  font-weight: 400;
  height: 30px;
  line-height: 30px;
  outline: none;
  vertical-align: middle;
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input:disabled {
  cursor: not-allowed;
  resize: block;
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color2);
}

.jp-InputGroup input:disabled ~ span {
  cursor: not-allowed;
  color: var(--jp-ui-font-color2);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color2);
}

.jp-InputGroupAction {
  position: absolute;
  bottom: 1px;
  right: 0;
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  font-family: var(--jp-ui-font-family);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

.jp-HTMLSelect.jp-DefaultStyle select:disabled {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color2);
  cursor: not-allowed;
  resize: block;
}

.jp-HTMLSelect.jp-DefaultStyle select:disabled ~ span {
  cursor: not-allowed;
}

/* Use our own theme for hover and option styles */
/* stylelint-disable-next-line selector-max-type */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}

select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-StatusBar-Widget {
  display: flex;
  align-items: center;
  background: var(--jp-layout-color2);
  min-height: var(--jp-statusbar-height);
  justify-content: space-between;
  padding: 0 10px;
}

.jp-StatusBar-Left {
  display: flex;
  align-items: center;
  flex-direction: row;
}

.jp-StatusBar-Middle {
  display: flex;
  align-items: center;
}

.jp-StatusBar-Right {
  display: flex;
  align-items: center;
  flex-direction: row-reverse;
}

.jp-StatusBar-Item {
  max-height: var(--jp-statusbar-height);
  margin: 0 2px;
  height: var(--jp-statusbar-height);
  white-space: nowrap;
  text-overflow: ellipsis;
  color: var(--jp-ui-font-color1);
  padding: 0 6px;
}

.jp-mod-highlighted:hover {
  background-color: var(--jp-layout-color3);
}

.jp-mod-clicked {
  background-color: var(--jp-brand-color1);
}

.jp-mod-clicked:hover {
  background-color: var(--jp-brand-color0);
}

.jp-mod-clicked .jp-StatusBar-TextItem {
  color: var(--jp-ui-inverse-font-color1);
}

.jp-StatusBar-HoverItem {
  box-shadow: '0px 4px 4px rgba(0, 0, 0, 0.25)';
}

.jp-StatusBar-TextItem {
  font-size: var(--jp-ui-font-size1);
  font-family: var(--jp-ui-font-family);
  line-height: 24px;
  color: var(--jp-ui-font-color1);
}

.jp-StatusBar-GroupItem {
  display: flex;
  align-items: center;
  flex-direction: row;
}

.jp-Statusbar-ProgressCircle svg {
  display: block;
  margin: 0 auto;
  width: 16px;
  height: 24px;
  align-self: normal;
}

.jp-Statusbar-ProgressCircle path {
  fill: var(--jp-inverse-layout-color3);
}

.jp-Statusbar-ProgressBar-progress-bar {
  height: 10px;
  width: 100px;
  border: solid 0.25px var(--jp-brand-color2);
  border-radius: 3px;
  overflow: hidden;
  align-self: center;
}

.jp-Statusbar-ProgressBar-progress-bar > div {
  background-color: var(--jp-brand-color2);
  background-image: linear-gradient(
    -45deg,
    rgba(255, 255, 255, 0.2) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.2) 50%,
    rgba(255, 255, 255, 0.2) 75%,
    transparent 75%,
    transparent
  );
  background-size: 40px 40px;
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 14px;
  color: #fff;
  text-align: center;
  animation: jp-Statusbar-ExecutionTime-progress-bar 2s linear infinite;
}

.jp-Statusbar-ProgressBar-progress-bar p {
  color: var(--jp-ui-font-color1);
  font-family: var(--jp-ui-font-family);
  font-size: var(--jp-ui-font-size1);
  line-height: 10px;
  width: 100px;
}

@keyframes jp-Statusbar-ExecutionTime-progress-bar {
  0% {
    background-position: 0 0;
  }

  100% {
    background-position: 40px 40px;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);

  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Modal variant
|----------------------------------------------------------------------------*/

.jp-ModalCommandPalette {
  position: absolute;
  z-index: 10000;
  top: 38px;
  left: 30%;
  margin: 0;
  padding: 4px;
  width: 40%;
  box-shadow: var(--jp-elevation-z4);
  border-radius: 4px;
  background: var(--jp-layout-color0);
}

.jp-ModalCommandPalette .lm-CommandPalette {
  max-height: 40vh;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-close-icon::after {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-header {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-item {
  margin-left: 4px;
  margin-right: 4px;
}

.jp-ModalCommandPalette
  .lm-CommandPalette
  .lm-CommandPalette-item.lm-mod-disabled {
  display: none;
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-SearchIconGroup {
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  padding: 5px 5px 1px;
}

.jp-SearchIconGroup svg {
  height: 20px;
  width: 20px;
}

.jp-SearchIconGroup .jp-icon3[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color2);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item.lm-mod-active {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active .jp-icon-selectable[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.6;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty::after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0;
  left: 0;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px 24px 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);

  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
  resize: both;
}

.jp-Dialog-content.jp-Dialog-content-small {
  max-width: 500px;
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-accept:focus,
button.jp-Dialog-button.jp-mod-styled.jp-mod-warn:focus,
button.jp-Dialog-button.jp-mod-styled.jp-mod-reject:focus {
  outline-offset: 4px;
  -moz-outline-radius: 0;
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-accept:focus {
  outline: 1px solid var(--jp-accept-color-normal, var(--jp-brand-color1));
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-warn:focus {
  outline: 1px solid var(--jp-warn-color-normal, var(--jp-error-color1));
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-reject:focus {
  outline: 1px solid var(--jp-reject-color-normal, var(--md-grey-600));
}

button.jp-Dialog-close-button {
  padding: 0;
  height: 100%;
  min-width: unset;
  min-height: unset;
}

.jp-Dialog-header {
  display: flex;
  justify-content: space-between;
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color1);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-checkbox {
  padding-right: 5px;
}

.jp-Dialog-checkbox > input:focus-visible {
  outline: 1px solid var(--jp-input-active-border-color);
  outline-offset: 1px;
}

.jp-Dialog-spacer {
  flex: 1 1 auto;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-Input-Boolean-Dialog {
  flex-direction: row-reverse;
  align-items: end;
  width: 100%;
}

.jp-Input-Boolean-Dialog > label {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

.jp-MainAreaWidget .jp-MainAreaWidget-error {
  padding: 6px;
}

.jp-MainAreaWidget .jp-MainAreaWidget-error > pre {
  width: auto;
  padding: 10px;
  background: var(--jp-error-color3);
  border: var(--jp-border-width) solid var(--jp-error-color1);
  border-radius: var(--jp-border-radius);
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  white-space: pre-wrap;
  word-wrap: break-word;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;
  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;
  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #a0f;
  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;
  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;
  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;
  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;
  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;
  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;
  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;
  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;
  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;
  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ff0;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;
  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;
  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;
  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;
  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;
  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;
  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

:root {
  /* This is the padding value to fill the gaps between lines containing spans with background color. */
  --jp-private-code-span-padding: calc(
    (var(--jp-code-line-height) - 1) * var(--jp-code-font-size) / 2
  );
}

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0;
  padding: 0;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}

.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}

.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}

.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}

.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}

.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}

.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}

.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}

.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}

.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}

.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}

.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}

.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}

.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}

.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}

.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}

.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);

  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

/* stylelint-disable selector-max-type, selector-max-compound-selectors */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0;
}

/* stylelint-enable selector-max-type, selector-max-compound-selectors */

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  table-layout: fixed;
  margin-left: auto;
  margin-bottom: 1em;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}

[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}

.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}

.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}

.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}

.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}

.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}

.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}

.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}

.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: var(--jp-ui-font-size0);
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-cursor-backdrop {
  position: fixed;
  width: 200px;
  height: 200px;
  margin-top: -100px;
  margin-left: -100px;
  will-change: transform;
  z-index: 100;
}

.lm-mod-drag-image {
  will-change: transform;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-lineFormSearch {
  padding: 4px 12px;
  background-color: var(--jp-layout-color2);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
  font-size: var(--jp-ui-font-size1);
}

.jp-lineFormCaption {
  font-size: var(--jp-ui-font-size0);
  line-height: var(--jp-ui-font-size1);
  margin-top: 4px;
  color: var(--jp-ui-font-color0);
}

.jp-baseLineForm {
  border: none;
  border-radius: 0;
  position: absolute;
  background-size: 16px;
  background-repeat: no-repeat;
  background-position: center;
  outline: none;
}

.jp-lineFormButtonContainer {
  top: 4px;
  right: 8px;
  height: 24px;
  padding: 0 12px;
  width: 12px;
}

.jp-lineFormButtonIcon {
  top: 0;
  right: 0;
  background-color: var(--jp-brand-color1);
  height: 100%;
  width: 100%;
  box-sizing: border-box;
  padding: 4px 6px;
}

.jp-lineFormButton {
  top: 0;
  right: 0;
  background-color: transparent;
  height: 100%;
  width: 100%;
  box-sizing: border-box;
}

.jp-lineFormWrapper {
  overflow: hidden;
  padding: 0 8px;
  border: 1px solid var(--jp-border-color0);
  background-color: var(--jp-input-active-background);
  height: 22px;
}

.jp-lineFormWrapperFocusWithin {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-lineFormInput {
  background: transparent;
  width: 200px;
  height: 100%;
  border: none;
  outline: none;
  color: var(--jp-ui-font-color0);
  line-height: 28px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/
.jp-DocumentSearch-input {
  border: none;
  outline: none;
  color: var(--jp-ui-font-color0);
  font-size: var(--jp-ui-font-size1);
  background-color: var(--jp-layout-color0);
  font-family: var(--jp-ui-font-family);
  padding: 2px 1px;
  resize: none;
}

.jp-DocumentSearch-overlay {
  position: absolute;
  background-color: var(--jp-toolbar-background);
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  border-left: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  top: 0;
  right: 0;
  z-index: 7;
  min-width: 405px;
  padding: 2px;
  font-size: var(--jp-ui-font-size1);

  --jp-private-document-search-button-height: 20px;
}

.jp-DocumentSearch-overlay button {
  background-color: var(--jp-toolbar-background);
  outline: 0;
}

.jp-DocumentSearch-overlay button:hover {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-overlay button:active {
  background-color: var(--jp-layout-color3);
}

.jp-DocumentSearch-overlay-row {
  display: flex;
  align-items: center;
  margin-bottom: 2px;
}

.jp-DocumentSearch-button-content {
  display: inline-block;
  cursor: pointer;
  box-sizing: border-box;
  width: 100%;
  height: 100%;
}

.jp-DocumentSearch-button-content svg {
  width: 100%;
  height: 100%;
}

.jp-DocumentSearch-input-wrapper {
  border: var(--jp-border-width) solid var(--jp-border-color0);
  display: flex;
  background-color: var(--jp-layout-color0);
  margin: 2px;
}

.jp-DocumentSearch-input-wrapper:focus-within {
  border-color: var(--jp-cell-editor-active-border-color);
}

.jp-DocumentSearch-toggle-wrapper,
.jp-DocumentSearch-button-wrapper {
  all: initial;
  overflow: hidden;
  display: inline-block;
  border: none;
  box-sizing: border-box;
}

.jp-DocumentSearch-toggle-wrapper {
  width: 14px;
  height: 14px;
}

.jp-DocumentSearch-button-wrapper {
  width: var(--jp-private-document-search-button-height);
  height: var(--jp-private-document-search-button-height);
}

.jp-DocumentSearch-toggle-wrapper:focus,
.jp-DocumentSearch-button-wrapper:focus {
  outline: var(--jp-border-width) solid
    var(--jp-cell-editor-active-border-color);
  outline-offset: -1px;
}

.jp-DocumentSearch-toggle-wrapper,
.jp-DocumentSearch-button-wrapper,
.jp-DocumentSearch-button-content:focus {
  outline: none;
}

.jp-DocumentSearch-toggle-placeholder {
  width: 5px;
}

.jp-DocumentSearch-input-button::before {
  display: block;
  padding-top: 100%;
}

.jp-DocumentSearch-input-button-off {
  opacity: var(--jp-search-toggle-off-opacity);
}

.jp-DocumentSearch-input-button-off:hover {
  opacity: var(--jp-search-toggle-hover-opacity);
}

.jp-DocumentSearch-input-button-on {
  opacity: var(--jp-search-toggle-on-opacity);
}

.jp-DocumentSearch-index-counter {
  padding-left: 10px;
  padding-right: 10px;
  user-select: none;
  min-width: 35px;
  display: inline-block;
}

.jp-DocumentSearch-up-down-wrapper {
  display: inline-block;
  padding-right: 2px;
  margin-left: auto;
  white-space: nowrap;
}

.jp-DocumentSearch-spacer {
  margin-left: auto;
}

.jp-DocumentSearch-up-down-wrapper button {
  outline: 0;
  border: none;
  width: var(--jp-private-document-search-button-height);
  height: var(--jp-private-document-search-button-height);
  vertical-align: middle;
  margin: 1px 5px 2px;
}

.jp-DocumentSearch-up-down-button:hover {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-up-down-button:active {
  background-color: var(--jp-layout-color3);
}

.jp-DocumentSearch-filter-button {
  border-radius: var(--jp-border-radius);
}

.jp-DocumentSearch-filter-button:hover {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-filter-button-enabled {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-filter-button-enabled:hover {
  background-color: var(--jp-layout-color3);
}

.jp-DocumentSearch-search-options {
  padding: 0 8px;
  margin-left: 3px;
  width: 100%;
  display: grid;
  justify-content: start;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  justify-items: stretch;
}

.jp-DocumentSearch-search-filter-disabled {
  color: var(--jp-ui-font-color2);
}

.jp-DocumentSearch-search-filter {
  display: flex;
  align-items: center;
  user-select: none;
}

.jp-DocumentSearch-regex-error {
  color: var(--jp-error-color0);
}

.jp-DocumentSearch-replace-button-wrapper {
  overflow: hidden;
  display: inline-block;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color0);
  margin: auto 2px;
  padding: 1px 4px;
  height: calc(var(--jp-private-document-search-button-height) + 2px);
}

.jp-DocumentSearch-replace-button-wrapper:focus {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
}

.jp-DocumentSearch-replace-button {
  display: inline-block;
  text-align: center;
  cursor: pointer;
  box-sizing: border-box;
  color: var(--jp-ui-font-color1);

  /* height - 2 * (padding of wrapper) */
  line-height: calc(var(--jp-private-document-search-button-height) - 2px);
  width: 100%;
  height: 100%;
}

.jp-DocumentSearch-replace-button:focus {
  outline: none;
}

.jp-DocumentSearch-replace-wrapper-class {
  margin-left: 14px;
  display: flex;
}

.jp-DocumentSearch-replace-toggle {
  border: none;
  background-color: var(--jp-toolbar-background);
  border-radius: var(--jp-border-radius);
}

.jp-DocumentSearch-replace-toggle:hover {
  background-color: var(--jp-layout-color2);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.cm-editor {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;

  /* Changed to auto to autogrow */
}

.cm-editor pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .cm-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

.jp-CodeMirrorEditor {
  cursor: text;
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .cm-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .cm-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.cm-editor.jp-mod-readOnly .cm-cursor {
  display: none;
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.cm-searching,
.cm-searching span {
  /* `.cm-searching span`: we need to override syntax highlighting */
  background-color: var(--jp-search-unselected-match-background-color);
  color: var(--jp-search-unselected-match-color);
}

.cm-searching::selection,
.cm-searching span::selection {
  background-color: var(--jp-search-unselected-match-background-color);
  color: var(--jp-search-unselected-match-color);
}

.jp-current-match > .cm-searching,
.jp-current-match > .cm-searching span,
.cm-searching > .jp-current-match,
.cm-searching > .jp-current-match span {
  background-color: var(--jp-search-selected-match-background-color);
  color: var(--jp-search-selected-match-color);
}

.jp-current-match > .cm-searching::selection,
.cm-searching > .jp-current-match::selection,
.jp-current-match > .cm-searching span::selection {
  background-color: var(--jp-search-selected-match-background-color);
  color: var(--jp-search-selected-match-color);
}

.cm-trailingspace {
  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAgAAAAFCAYAAAB4ka1VAAAAsElEQVQIHQGlAFr/AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA7+r3zKmT0/+pk9P/7+r3zAAAAAAAAAAABAAAAAAAAAAA6OPzM+/q9wAAAAAA6OPzMwAAAAAAAAAAAgAAAAAAAAAAGR8NiRQaCgAZIA0AGR8NiQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQyoYJ/SY80UAAAAASUVORK5CYII=);
  background-position: center left;
  background-repeat: repeat-x;
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/* Styles for shared cursors (remote cursor locations and selected ranges) */
.jp-CodeMirrorEditor .cm-ySelectionCaret {
  position: relative;
  border-left: 1px solid black;
  margin-left: -1px;
  margin-right: -1px;
  box-sizing: border-box;
}

.jp-CodeMirrorEditor .cm-ySelectionCaret > .cm-ySelectionInfo {
  white-space: nowrap;
  position: absolute;
  top: -1.15em;
  padding-bottom: 0.05em;
  left: -1px;
  font-size: 0.95em;
  font-family: var(--jp-ui-font-family);
  font-weight: bold;
  line-height: normal;
  user-select: none;
  color: white;
  padding-left: 2px;
  padding-right: 2px;
  z-index: 101;
  transition: opacity 0.3s ease-in-out;
}

.jp-CodeMirrorEditor .cm-ySelectionInfo {
  transition-delay: 0.7s;
  opacity: 0;
}

.jp-CodeMirrorEditor .cm-ySelectionCaret:hover > .cm-ySelectionInfo {
  opacity: 1;
  transition-delay: 0s;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser .jp-SidePanel-content {
  display: flex;
  flex-direction: column;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  flex-wrap: wrap;
  row-gap: 12px;
  border-bottom: none;
  height: auto;
  margin: 8px 12px 0;
  box-shadow: none;
  padding: 0;
  justify-content: flex-start;
}

.jp-FileBrowser-Panel {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 8px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0 2px;
  padding: 0 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  padding-left: 0;
  padding-right: 2px;
  align-items: center;
  height: unset;
}

.jp-FileBrowser-toolbar > .jp-Toolbar-item .jp-ToolbarButtonComponent {
  width: 40px;
}

/*-----------------------------------------------------------------------------
| Other styles
|----------------------------------------------------------------------------*/

.jp-FileDialog.jp-mod-conflict input {
  color: var(--jp-error-color1);
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

.jp-LastModified-hidden {
  display: none;
}

.jp-FileSize-hidden {
  display: none;
}

.jp-FileBrowser .lm-AccordionPanel > h3:first-child {
  display: none;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-DirListing-headerItem.jp-id-filesize {
  flex: 0 0 75px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-id-narrow {
  display: none;
  flex: 0 0 5px;
  padding: 4px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
  color: var(--jp-border-color2);
}

.jp-DirListing-narrow .jp-id-narrow {
  display: block;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-content mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.jp-DirListing-content .jp-DirListing-item.jp-mod-selected mark {
  color: var(--jp-ui-inverse-font-color0);
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-checkboxWrapper {
  /* Increases hit area of checkbox. */
  padding: 4px;
}

.jp-DirListing-header
  .jp-DirListing-checkboxWrapper
  + .jp-DirListing-headerItem {
  padding-left: 4px;
}

.jp-DirListing-content .jp-DirListing-checkboxWrapper {
  position: relative;
  left: -4px;
  margin: -4px 0 -4px -8px;
}

.jp-DirListing-checkboxWrapper.jp-mod-visible {
  visibility: visible;
}

/* For devices that support hovering, hide checkboxes until hovered, selected...
*/
@media (hover: hover) {
  .jp-DirListing-checkboxWrapper {
    visibility: hidden;
  }

  .jp-DirListing-item:hover .jp-DirListing-checkboxWrapper,
  .jp-DirListing-item.jp-mod-selected .jp-DirListing-checkboxWrapper {
    visibility: visible;
  }
}

.jp-DirListing-item[data-is-dot] {
  opacity: 75%;
}

.jp-DirListing-item.jp-mod-selected {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemText:focus {
  outline-width: 2px;
  outline-color: var(--jp-inverse-layout-color1);
  outline-style: solid;
  outline-offset: 1px;
}

.jp-DirListing-item.jp-mod-selected .jp-DirListing-itemText:focus {
  outline-color: var(--jp-layout-color1);
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-itemFileSize {
  flex: 0 0 90px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon::before {
  color: var(--jp-success-color1);
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.jp-mod-running.jp-mod-selected
  .jp-DirListing-itemIcon::before {
  color: var(--jp-ui-inverse-font-color1);
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: table;
  table-layout: fixed;
  width: 100%;
  overflow: hidden;
}

.jp-OutputPrompt {
  width: var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);

  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;

  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-OutputArea-prompt {
  display: table-cell;
  vertical-align: top;
}

.jp-OutputArea-output {
  display: table-cell;
  width: 100%;
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea .jp-RenderedText {
  padding-left: 1ch;
}

/**
 * Prompt overlay.
 */

.jp-OutputArea-promptOverlay {
  position: absolute;
  top: 0;
  width: var(--jp-cell-prompt-width);
  height: 100%;
  opacity: 0.5;
}

.jp-OutputArea-promptOverlay:hover {
  background: var(--jp-layout-color2);
  box-shadow: inset 0 0 1px var(--jp-inverse-layout-color0);
  cursor: zoom-out;
}

.jp-mod-outputsScrolled .jp-OutputArea-promptOverlay:hover {
  cursor: zoom-in;
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `lm-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0;
  padding: 0;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

.jp-TrimmedOutputs pre {
  background: var(--jp-layout-color3);
  font-size: calc(var(--jp-code-font-size) * 1.4);
  text-align: center;
  text-transform: uppercase;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/* Hide empty lines in the output area, for instance due to cleared widgets */
.jp-OutputArea-prompt:empty {
  padding: 0;
  border: 0;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0;
  width: 100%;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
  border-top: var(--jp-border-width) solid transparent;
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;

  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;

  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0 0.25em;
  margin: 0 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input::placeholder {
  opacity: 0;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

.jp-Stdin-input:focus::placeholder {
  opacity: 1;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Printing
|----------------------------------------------------------------------------*/

@media print {
  .jp-OutputArea-child {
    break-inside: avoid-page;
  }
}

/*-----------------------------------------------------------------------------
| Mobile
|----------------------------------------------------------------------------*/
@media only screen and (max-width: 760px) {
  .jp-OutputPrompt {
    display: table-row;
    text-align: left;
  }

  .jp-OutputArea-child .jp-OutputArea-output {
    display: table-row;
    margin-left: var(--jp-notebook-padding);
  }
}

/* Trimmed outputs warning */
.jp-TrimmedOutputs > a {
  margin: 10px;
  text-decoration: none;
  cursor: pointer;
}

.jp-TrimmedOutputs > a:hover {
  text-decoration: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Table of Contents
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toc-active-width: 4px;
}

.jp-TableOfContents {
  display: flex;
  flex-direction: column;
  background: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  height: 100%;
}

.jp-TableOfContents-placeholder {
  text-align: center;
}

.jp-TableOfContents-placeholderContent {
  color: var(--jp-content-font-color2);
  padding: 8px;
}

.jp-TableOfContents-placeholderContent > h3 {
  margin-bottom: var(--jp-content-heading-margin-bottom);
}

.jp-TableOfContents .jp-SidePanel-content {
  overflow-y: auto;
}

.jp-TableOfContents-tree {
  margin: 4px;
}

.jp-TableOfContents ol {
  list-style-type: none;
}

/* stylelint-disable-next-line selector-max-type */
.jp-TableOfContents li > ol {
  /* Align left border with triangle icon center */
  padding-left: 11px;
}

.jp-TableOfContents-content {
  /* left margin for the active heading indicator */
  margin: 0 0 0 var(--jp-private-toc-active-width);
  padding: 0;
  background-color: var(--jp-layout-color1);
}

.jp-tocItem {
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-tocItem-heading {
  display: flex;
  cursor: pointer;
}

.jp-tocItem-heading:hover {
  background-color: var(--jp-layout-color2);
}

.jp-tocItem-content {
  display: block;
  padding: 4px 0;
  white-space: nowrap;
  text-overflow: ellipsis;
  overflow-x: hidden;
}

.jp-tocItem-collapser {
  height: 20px;
  margin: 2px 2px 0;
  padding: 0;
  background: none;
  border: none;
  cursor: pointer;
}

.jp-tocItem-collapser:hover {
  background-color: var(--jp-layout-color3);
}

/* Active heading indicator */

.jp-tocItem-heading::before {
  content: ' ';
  background: transparent;
  width: var(--jp-private-toc-active-width);
  height: 24px;
  position: absolute;
  left: 0;
  border-radius: var(--jp-border-radius);
}

.jp-tocItem-heading.jp-tocItem-active::before {
  background-color: var(--jp-brand-color1);
}

.jp-tocItem-heading:hover.jp-tocItem-active::before {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0;
  margin: 0;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;

  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0;
  bottom: 0;
}

/*-----------------------------------------------------------------------------
| Printing
|----------------------------------------------------------------------------*/

/*
Hiding collapsers in print mode.

Note: input and output wrappers have "display: block" propery in print mode.
*/

@media print {
  .jp-Collapser {
    display: none;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0;
  width: 100%;
  padding: 0;
  margin: 0;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: table;
  table-layout: fixed;
  width: 100%;
  overflow: hidden;
}

.jp-InputArea-editor {
  display: table-cell;
  overflow: hidden;
  vertical-align: top;

  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0;
  background: var(--jp-cell-editor-background);
}

.jp-InputPrompt {
  display: table-cell;
  vertical-align: top;
  width: var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;

  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;

  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/*-----------------------------------------------------------------------------
| Mobile
|----------------------------------------------------------------------------*/
@media only screen and (max-width: 760px) {
  .jp-InputArea-editor {
    display: table-row;
    margin-left: var(--jp-notebook-padding);
  }

  .jp-InputPrompt {
    display: table-row;
    text-align: left;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: table;
  table-layout: fixed;
  width: 100%;
}

.jp-Placeholder-prompt {
  display: table-cell;
  box-sizing: border-box;
}

.jp-Placeholder-content {
  display: table-cell;
  padding: 4px 6px;
  border: 1px solid transparent;
  border-radius: 0;
  background: none;
  box-sizing: border-box;
  cursor: pointer;
}

.jp-Placeholder-contentContainer {
  display: flex;
}

.jp-Placeholder-content:hover,
.jp-InputPlaceholder > .jp-Placeholder-content:hover {
  border-color: var(--jp-layout-color3);
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0 0 2px 0 rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

.jp-PlaceholderText {
  white-space: nowrap;
  overflow-x: hidden;
  color: var(--jp-inverse-layout-color3);
  font-family: var(--jp-code-font-family);
}

.jp-InputPlaceholder > .jp-Placeholder-content {
  border-color: var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0;
  margin: 0;

  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 24em;
  margin-left: var(--jp-private-cell-scrolling-output-offset);
  resize: vertical;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea[style*='height'] {
  max-height: unset;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea::after {
  content: ' ';
  box-shadow: inset 0 0 6px 2px rgb(0 0 0 / 30%);
  width: 100%;
  height: 100%;
  position: sticky;
  bottom: 0;
  top: 0;
  margin-top: -50%;
  float: left;
  display: block;
  pointer-events: none;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-child {
  padding-top: 6px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  width: calc(
    var(--jp-cell-prompt-width) - var(--jp-private-cell-scrolling-output-offset)
  );
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-promptOverlay {
  left: calc(-1 * var(--jp-private-cell-scrolling-output-offset));
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  display: table-cell;
  width: 100%;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

/* collapseHeadingButton (show always if hiddenCellsButton is _not_ shown) */
.jp-collapseHeadingButton {
  display: flex;
  min-height: var(--jp-cell-collapser-min-height);
  font-size: var(--jp-code-font-size);
  position: absolute;
  background-color: transparent;
  background-size: 25px;
  background-repeat: no-repeat;
  background-position-x: center;
  background-position-y: top;
  background-image: var(--jp-icon-caret-down);
  right: 0;
  top: 0;
  bottom: 0;
}

.jp-collapseHeadingButton.jp-mod-collapsed {
  background-image: var(--jp-icon-caret-right);
}

/*
 set the container font size to match that of content
 so that the nested collapse buttons have the right size
*/
.jp-MarkdownCell .jp-InputPrompt {
  font-size: var(--jp-content-font-size1);
}

/*
  Align collapseHeadingButton with cell top header
  The font sizes are identical to the ones in packages/rendermime/style/base.css
*/
.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='1'] {
  font-size: var(--jp-content-font-size5);
  background-position-y: calc(0.3 * var(--jp-content-font-size5));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='2'] {
  font-size: var(--jp-content-font-size4);
  background-position-y: calc(0.3 * var(--jp-content-font-size4));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='3'] {
  font-size: var(--jp-content-font-size3);
  background-position-y: calc(0.3 * var(--jp-content-font-size3));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='4'] {
  font-size: var(--jp-content-font-size2);
  background-position-y: calc(0.3 * var(--jp-content-font-size2));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='5'] {
  font-size: var(--jp-content-font-size1);
  background-position-y: top;
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='6'] {
  font-size: var(--jp-content-font-size0);
  background-position-y: top;
}

/* collapseHeadingButton (show only on (hover,active) if hiddenCellsButton is shown) */
.jp-Notebook.jp-mod-showHiddenCellsButton .jp-collapseHeadingButton {
  display: none;
}

.jp-Notebook.jp-mod-showHiddenCellsButton
  :is(.jp-MarkdownCell:hover, .jp-mod-active)
  .jp-collapseHeadingButton {
  display: flex;
}

/* showHiddenCellsButton (only show if jp-mod-showHiddenCellsButton is set, which
is a consequence of the showHiddenCellsButton option in Notebook Settings)*/
.jp-Notebook.jp-mod-showHiddenCellsButton .jp-showHiddenCellsButton {
  margin-left: calc(var(--jp-cell-prompt-width) + 2 * var(--jp-code-padding));
  margin-top: var(--jp-code-padding);
  border: 1px solid var(--jp-border-color2);
  background-color: var(--jp-border-color3) !important;
  color: var(--jp-content-font-color0) !important;
  display: flex;
}

.jp-Notebook.jp-mod-showHiddenCellsButton .jp-showHiddenCellsButton:hover {
  background-color: var(--jp-border-color2) !important;
}

.jp-showHiddenCellsButton {
  display: none;
}

/*-----------------------------------------------------------------------------
| Printing
|----------------------------------------------------------------------------*/

/*
Using block instead of flex to allow the use of the break-inside CSS property for
cell outputs.
*/

@media print {
  .jp-Cell-inputWrapper,
  .jp-Cell-outputWrapper {
    display: block;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-notebook-toolbar-padding: 2px 5px 2px 2px;
}

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: var(--jp-notebook-toolbar-padding);

  /* disable paint containment from lumino 2.0 default strict CSS containment */
  contain: style size !important;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

.jp-Toolbar-responsive-popup {
  position: absolute;
  height: fit-content;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: flex-end;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: var(--jp-notebook-toolbar-padding);
  z-index: 1;
  right: 0;
  top: 0;
}

.jp-Toolbar > .jp-Toolbar-responsive-opener {
  margin-left: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-Notebook-ExecutionIndicator {
  position: relative;
  display: inline-block;
  height: 100%;
  z-index: 9997;
}

.jp-Notebook-ExecutionIndicator-tooltip {
  visibility: hidden;
  height: auto;
  width: max-content;
  width: -moz-max-content;
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color1);
  text-align: justify;
  border-radius: 6px;
  padding: 0 5px;
  position: fixed;
  display: table;
}

.jp-Notebook-ExecutionIndicator-tooltip.up {
  transform: translateX(-50%) translateY(-100%) translateY(-32px);
}

.jp-Notebook-ExecutionIndicator-tooltip.down {
  transform: translateX(calc(-100% + 16px)) translateY(5px);
}

.jp-Notebook-ExecutionIndicator-tooltip.hidden {
  display: none;
}

.jp-Notebook-ExecutionIndicator:hover .jp-Notebook-ExecutionIndicator-tooltip {
  visibility: visible;
}

.jp-Notebook-ExecutionIndicator span {
  font-size: var(--jp-ui-font-size1);
  font-family: var(--jp-ui-font-family);
  color: var(--jp-ui-font-color1);
  line-height: 24px;
  display: block;
}

.jp-Notebook-ExecutionIndicator-progress-bar {
  display: flex;
  justify-content: center;
  height: 100%;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*
 * Execution indicator
 */
.jp-tocItem-content::after {
  content: '';

  /* Must be identical to form a circle */
  width: 12px;
  height: 12px;
  background: none;
  border: none;
  position: absolute;
  right: 0;
}

.jp-tocItem-content[data-running='0']::after {
  border-radius: 50%;
  border: var(--jp-border-width) solid var(--jp-inverse-layout-color3);
  background: none;
}

.jp-tocItem-content[data-running='1']::after {
  border-radius: 50%;
  border: var(--jp-border-width) solid var(--jp-inverse-layout-color3);
  background-color: var(--jp-inverse-layout-color3);
}

.jp-tocItem-content[data-running='0'],
.jp-tocItem-content[data-running='1'] {
  margin-right: 12px;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-Notebook-footer {
  height: 27px;
  margin-left: calc(
    var(--jp-cell-prompt-width) + var(--jp-cell-collapser-width) +
      var(--jp-cell-padding)
  );
  width: calc(
    100% -
      (
        var(--jp-cell-prompt-width) + var(--jp-cell-collapser-width) +
          var(--jp-cell-padding) + var(--jp-cell-padding)
      )
  );
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  color: var(--jp-ui-font-color3);
  margin-top: 6px;
  background: none;
  cursor: pointer;
}

.jp-Notebook-footer:focus {
  border-color: var(--jp-cell-editor-active-border-color);
}

/* For devices that support hovering, hide footer until hover */
@media (hover: hover) {
  .jp-Notebook-footer {
    opacity: 0;
  }

  .jp-Notebook-footer:focus,
  .jp-Notebook-footer:hover {
    opacity: 1;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-side-by-side-output-size: 1fr;
  --jp-side-by-side-resized-cell: var(--jp-side-by-side-output-size);
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

/* stylelint-disable selector-max-class */

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-MainAreaWidget-ContainStrict .jp-Notebook * {
  contain: strict;
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* cell is dirty */
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt {
  color: var(--jp-warn-color1);
}

.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt::before {
  color: var(--jp-warn-color1);
  content: '•';
}

.jp-Notebook .jp-Cell.jp-mod-active.jp-mod-dirty .jp-Collapser {
  background: var(--jp-warn-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: block;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0 rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0 rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);

  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-ActiveCellTool {
  padding: 12px 0;
  display: flex;
}

.jp-ActiveCellTool-Content {
  flex: 1 1 auto;
}

.jp-ActiveCellTool .jp-ActiveCellTool-CellContent {
  background: var(--jp-cell-editor-background);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0;
  min-height: 29px;
}

.jp-ActiveCellTool .jp-InputPrompt {
  min-width: calc(var(--jp-cell-prompt-width) * 0.75);
}

.jp-ActiveCellTool-CellContent > pre {
  padding: 5px 4px;
  margin: 0;
  white-space: normal;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label,
.jp-NumberSetter label {
  line-height: 1.4;
}

.jp-NotebookTools .jp-select-wrapper {
  margin-top: 4px;
  margin-bottom: 0;
}

.jp-NumberSetter input {
  width: 100%;
  margin-top: 4px;
}

.jp-NotebookTools .jp-Collapse {
  margin-top: 16px;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

/*-----------------------------------------------------------------------------
| Side-by-side Mode (.jp-mod-sideBySide)
|----------------------------------------------------------------------------*/
.jp-mod-sideBySide.jp-Notebook .jp-Notebook-cell {
  margin-top: 3em;
  margin-bottom: 3em;
  margin-left: 5%;
  margin-right: 5%;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell {
  display: grid;
  grid-template-columns: minmax(0, 1fr) min-content minmax(
      0,
      var(--jp-side-by-side-output-size)
    );
  grid-template-rows: auto minmax(0, 1fr) auto;
  grid-template-areas:
    'header header header'
    'input handle output'
    'footer footer footer';
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell.jp-mod-resizedCell {
  grid-template-columns: minmax(0, 1fr) min-content minmax(
      0,
      var(--jp-side-by-side-resized-cell)
    );
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellHeader {
  grid-area: header;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-Cell-inputWrapper {
  grid-area: input;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-Cell-outputWrapper {
  /* overwrite the default margin (no vertical separation needed in side by side move */
  margin-top: 0;
  grid-area: output;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellFooter {
  grid-area: footer;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellResizeHandle {
  grid-area: handle;
  user-select: none;
  display: block;
  height: 100%;
  cursor: ew-resize;
  padding: 0 var(--jp-cell-padding);
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellResizeHandle::after {
  content: '';
  display: block;
  background: var(--jp-border-color2);
  height: 100%;
  width: 5px;
}

.jp-mod-sideBySide.jp-Notebook
  .jp-CodeCell.jp-mod-resizedCell
  .jp-CellResizeHandle::after {
  background: var(--jp-border-color0);
}

.jp-CellResizeHandle {
  display: none;
}

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Cell-Placeholder {
  padding-left: 55px;
}

.jp-Cell-Placeholder-wrapper {
  background: #fff;
  border: 1px solid;
  border-color: #e5e6e9 #dfe0e4 #d0d1d5;
  border-radius: 4px;
  -webkit-border-radius: 4px;
  margin: 10px 15px;
}

.jp-Cell-Placeholder-wrapper-inner {
  padding: 15px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body {
  background-repeat: repeat;
  background-size: 50% auto;
}

.jp-Cell-Placeholder-wrapper-body div {
  background: #f6f7f8;
  background-image: -webkit-linear-gradient(
    left,
    #f6f7f8 0%,
    #edeef1 20%,
    #f6f7f8 40%,
    #f6f7f8 100%
  );
  background-repeat: no-repeat;
  background-size: 800px 104px;
  height: 104px;
  position: absolute;
  right: 15px;
  left: 15px;
  top: 15px;
}

div.jp-Cell-Placeholder-h1 {
  top: 20px;
  height: 20px;
  left: 15px;
  width: 150px;
}

div.jp-Cell-Placeholder-h2 {
  left: 15px;
  top: 50px;
  height: 10px;
  width: 100px;
}

div.jp-Cell-Placeholder-content-1,
div.jp-Cell-Placeholder-content-2,
div.jp-Cell-Placeholder-content-3 {
  left: 15px;
  right: 15px;
  height: 10px;
}

div.jp-Cell-Placeholder-content-1 {
  top: 100px;
}

div.jp-Cell-Placeholder-content-2 {
  top: 120px;
}

div.jp-Cell-Placeholder-content-3 {
  top: 140px;
}

</style>
<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0 2px 1px -1px var(--jp-shadow-umbra-color),
    0 1px 1px 0 var(--jp-shadow-penumbra-color),
    0 1px 3px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0 3px 1px -2px var(--jp-shadow-umbra-color),
    0 2px 2px 0 var(--jp-shadow-penumbra-color),
    0 1px 5px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0 2px 4px -1px var(--jp-shadow-umbra-color),
    0 4px 5px 0 var(--jp-shadow-penumbra-color),
    0 1px 10px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0 3px 5px -1px var(--jp-shadow-umbra-color),
    0 6px 10px 0 var(--jp-shadow-penumbra-color),
    0 1px 18px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0 5px 5px -3px var(--jp-shadow-umbra-color),
    0 8px 10px 1px var(--jp-shadow-penumbra-color),
    0 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0 7px 8px -4px var(--jp-shadow-umbra-color),
    0 12px 17px 2px var(--jp-shadow-penumbra-color),
    0 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0 8px 10px -5px var(--jp-shadow-umbra-color),
    0 16px 24px 2px var(--jp-shadow-penumbra-color),
    0 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0 10px 13px -6px var(--jp-shadow-umbra-color),
    0 20px 31px 3px var(--jp-shadow-penumbra-color),
    0 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0 11px 15px -7px var(--jp-shadow-umbra-color),
    0 24px 38px 3px var(--jp-shadow-penumbra-color),
    0 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-inverse-border-color: var(--md-grey-600);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;
  --jp-ui-font-family: system-ui, -apple-system, blinkmacsystemfont, 'Segoe UI',
    helvetica, arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;
  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);
  --jp-content-link-color: var(--md-blue-900);
  --jp-content-font-family: system-ui, -apple-system, blinkmacsystemfont,
    'Segoe UI', helvetica, arial, sans-serif, 'Apple Color Emoji',
    'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: menlo, consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-900);
  --jp-brand-color1: var(--md-blue-700);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);
  --jp-accent-color0: var(--md-green-900);
  --jp-accent-color1: var(--md-green-700);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-900);
  --jp-warn-color1: var(--md-orange-700);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);
  --jp-error-color0: var(--md-red-900);
  --jp-error-color1: var(--md-red-700);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);
  --jp-success-color0: var(--md-green-900);
  --jp-success-color1: var(--md-green-700);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);
  --jp-info-color0: var(--md-cyan-900);
  --jp-info-color1: var(--md-cyan-700);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;
  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;
  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);
  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: var(--jp-code-font-family-default);
  --jp-cell-prompt-letter-spacing: 0;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);

  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;

  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0 0 2px 0 rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Statusbar specific styles */

  --jp-statusbar-height: 24px;

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-inverse-border-color);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #008000;
  --jp-mirror-editor-atom-color: #88f;
  --jp-mirror-editor-number-color: #080;
  --jp-mirror-editor-def-color: #00f;
  --jp-mirror-editor-variable-color: var(--md-grey-900);
  --jp-mirror-editor-variable-2-color: rgb(0, 54, 109);
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #a2f;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #a2f;
  --jp-mirror-editor-qualifier-color: #555;
  --jp-mirror-editor-builtin-color: #008000;
  --jp-mirror-editor-bracket-color: #997;
  --jp-mirror-editor-tag-color: #170;
  --jp-mirror-editor-attribute-color: #00c;
  --jp-mirror-editor-header-color: blue;
  --jp-mirror-editor-quote-color: #090;
  --jp-mirror-editor-link-color: #00c;
  --jp-mirror-editor-error-color: #f00;
  --jp-mirror-editor-hr-color: #999;

  /*
    RTC user specific colors.
    These colors are used for the cursor, username in the editor,
    and the icon of the user.
  */

  --jp-collaborator-color1: #ffad8e;
  --jp-collaborator-color2: #dac83d;
  --jp-collaborator-color3: #72dd76;
  --jp-collaborator-color4: #00e4d0;
  --jp-collaborator-color5: #45d4ff;
  --jp-collaborator-color6: #e2b1ff;
  --jp-collaborator-color7: #ff9de6;

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 250px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);

  /* Button colors */
  --jp-accept-color-normal: var(--md-blue-700);
  --jp-accept-color-hover: var(--md-blue-800);
  --jp-accept-color-active: var(--md-blue-900);
  --jp-warn-color-normal: var(--md-red-700);
  --jp-warn-color-hover: var(--md-red-800);
  --jp-warn-color-active: var(--md-red-900);
  --jp-reject-color-normal: var(--md-grey-600);
  --jp-reject-color-hover: var(--md-grey-700);
  --jp-reject-color-active: var(--md-grey-800);

  /* File or activity icons and switch semantic variables */
  --jp-jupyter-icon-color: #f37626;
  --jp-notebook-icon-color: #f37626;
  --jp-json-icon-color: var(--md-orange-700);
  --jp-console-icon-background-color: var(--md-blue-700);
  --jp-console-icon-color: white;
  --jp-terminal-icon-background-color: var(--md-grey-800);
  --jp-terminal-icon-color: var(--md-grey-200);
  --jp-text-editor-icon-color: var(--md-grey-700);
  --jp-inspector-icon-color: var(--md-grey-700);
  --jp-switch-color: var(--md-grey-400);
  --jp-switch-true-position-color: var(--md-orange-900);
}
</style>
<style type="text/css">
/* Force rendering true colors when outputing to pdf */
* {
  -webkit-print-color-adjust: exact;
}

/* Misc */
a.anchor-link {
  display: none;
}

/* Input area styling */
.jp-InputArea {
  overflow: hidden;
}

.jp-InputArea-editor {
  overflow: hidden;
}

.cm-editor.cm-s-jupyter .highlight pre {
/* weird, but --jp-code-padding defined to be 5px but 4px horizontal padding is hardcoded for pre.cm-line */
  padding: var(--jp-code-padding) 4px;
  margin: 0;

  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
  color: inherit;

}

.jp-OutputArea-output pre {
  line-height: inherit;
  font-family: inherit;
}

.jp-RenderedText pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
}

/* Hiding the collapser by default */
.jp-Collapser {
  display: none;
}

@page {
    margin: 0.5in; /* Margin for each printed piece of paper */
}

@media print {
  .jp-Cell-inputWrapper,
  .jp-Cell-outputWrapper {
    display: block;
  }
}
</style>
<!-- Load mathjax -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-AMS_CHTML-full,Safe"> </script>
<!-- MathJax configuration -->
<script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: {
                    automatic: true
                    }
                }
            });

            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
<!-- End of mathjax configuration --><script type="module">
  document.addEventListener("DOMContentLoaded", async () => {
    const diagrams = document.querySelectorAll(".jp-Mermaid > pre.mermaid");
    // do not load mermaidjs if not needed
    if (!diagrams.length) {
      return;
    }
    const mermaid = (await import("https://cdnjs.cloudflare.com/ajax/libs/mermaid/10.7.0/mermaid.esm.min.mjs")).default;
    const parser = new DOMParser();

    mermaid.initialize({
      maxTextSize: 100000,
      maxEdges: 100000,
      startOnLoad: false,
      fontFamily: window
        .getComputedStyle(document.body)
        .getPropertyValue("--jp-ui-font-family"),
      theme: document.querySelector("body[data-jp-theme-light='true']")
        ? "default"
        : "dark",
    });

    let _nextMermaidId = 0;

    function makeMermaidImage(svg) {
      const img = document.createElement("img");
      const doc = parser.parseFromString(svg, "image/svg+xml");
      const svgEl = doc.querySelector("svg");
      const { maxWidth } = svgEl?.style || {};
      const firstTitle = doc.querySelector("title");
      const firstDesc = doc.querySelector("desc");

      img.setAttribute("src", `data:image/svg+xml,${encodeURIComponent(svg)}`);
      if (maxWidth) {
        img.width = parseInt(maxWidth);
      }
      if (firstTitle) {
        img.setAttribute("alt", firstTitle.textContent);
      }
      if (firstDesc) {
        const caption = document.createElement("figcaption");
        caption.className = "sr-only";
        caption.textContent = firstDesc.textContent;
        return [img, caption];
      }
      return [img];
    }

    async function makeMermaidError(text) {
      let errorMessage = "";
      try {
        await mermaid.parse(text);
      } catch (err) {
        errorMessage = `${err}`;
      }

      const result = document.createElement("details");
      result.className = 'jp-RenderedMermaid-Details';
      const summary = document.createElement("summary");
      summary.className = 'jp-RenderedMermaid-Summary';
      const pre = document.createElement("pre");
      const code = document.createElement("code");
      code.innerText = text;
      pre.appendChild(code);
      summary.appendChild(pre);
      result.appendChild(summary);

      const warning = document.createElement("pre");
      warning.innerText = errorMessage;
      result.appendChild(warning);
      return [result];
    }

    async function renderOneMarmaid(src) {
      const id = `jp-mermaid-${_nextMermaidId++}`;
      const parent = src.parentNode;
      let raw = src.textContent.trim();
      const el = document.createElement("div");
      el.style.visibility = "hidden";
      document.body.appendChild(el);
      let results = null;
      let output = null;
      try {
        let { svg } = await mermaid.render(id, raw, el);
        svg = cleanMermaidSvg(svg);
        results = makeMermaidImage(svg);
        output = document.createElement("figure");
        results.map(output.appendChild, output);
      } catch (err) {
        parent.classList.add("jp-mod-warning");
        results = await makeMermaidError(raw);
        output = results[0];
      } finally {
        el.remove();
      }
      parent.classList.add("jp-RenderedMermaid");
      parent.appendChild(output);
    }


    /**
     * Post-process to ensure mermaid diagrams contain only valid SVG and XHTML.
     */
    function cleanMermaidSvg(svg) {
      return svg.replace(RE_VOID_ELEMENT, replaceVoidElement);
    }


    /**
     * A regular expression for all void elements, which may include attributes and
     * a slash.
     *
     * @see https://developer.mozilla.org/en-US/docs/Glossary/Void_element
     *
     * Of these, only `<br>` is generated by Mermaid in place of `\n`,
     * but _any_ "malformed" tag will break the SVG rendering entirely.
     */
    const RE_VOID_ELEMENT =
      /<\s*(area|base|br|col|embed|hr|img|input|link|meta|param|source|track|wbr)\s*([^>]*?)\s*>/gi;

    /**
     * Ensure a void element is closed with a slash, preserving any attributes.
     */
    function replaceVoidElement(match, tag, rest) {
      rest = rest.trim();
      if (!rest.endsWith('/')) {
        rest = `${rest} /`;
      }
      return `<${tag} ${rest}>`;
    }

    void Promise.all([...diagrams].map(renderOneMarmaid));
  });
</script>
<style>
  .jp-Mermaid:not(.jp-RenderedMermaid) {
    display: none;
  }

  .jp-RenderedMermaid {
    overflow: auto;
    display: flex;
  }

  .jp-RenderedMermaid.jp-mod-warning {
    width: auto;
    padding: 0.5em;
    margin-top: 0.5em;
    border: var(--jp-border-width) solid var(--jp-warn-color2);
    border-radius: var(--jp-border-radius);
    color: var(--jp-ui-font-color1);
    font-size: var(--jp-ui-font-size1);
    white-space: pre-wrap;
    word-wrap: break-word;
  }

  .jp-RenderedMermaid figure {
    margin: 0;
    overflow: auto;
    max-width: 100%;
  }

  .jp-RenderedMermaid img {
    max-width: 100%;
  }

  .jp-RenderedMermaid-Details > pre {
    margin-top: 1em;
  }

  .jp-RenderedMermaid-Summary {
    color: var(--jp-warn-color2);
  }

  .jp-RenderedMermaid:not(.jp-mod-warning) pre {
    display: none;
  }

  .jp-RenderedMermaid-Summary > pre {
    display: inline-block;
    white-space: normal;
  }
</style>
<!-- End of mermaid configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">
<main><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1">#MarketMentorAI</span>
<span class="c1"># Import packages</span>
<span class="o">%</span><span class="k">pip</span> install yfinance
<span class="o">%</span><span class="k">pip</span> install yahoo_fin
<span class="o">%</span><span class="k">pip</span> install scikit-learn
<span class="o">%</span><span class="k">pip</span> install matplotlib
<span class="o">%</span><span class="k">pip</span> install textblob
<span class="o">%</span><span class="k">pip</span> install seaborn
<span class="o">%</span><span class="k">pip</span> install PyPortfolioOpt
<span class="o">%</span><span class="k">pip</span> install statsmodels
<span class="o">%</span><span class="k">pip</span> install tqdm

<span class="c1"># Import packages</span>
<span class="kn">import</span> <span class="nn">yfinance</span> <span class="k">as</span> <span class="nn">yf</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">from</span> <span class="nn">yahoo_fin</span> <span class="kn">import</span> <span class="n">stock_info</span>
<span class="kn">from</span> <span class="nn">yahoo_fin.stock_info</span> <span class="kn">import</span> <span class="n">get_analysts_info</span>
<span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="kn">import</span> <span class="n">RandomForestRegressor</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">from</span> <span class="nn">sklearn.preprocessing</span> <span class="kn">import</span> <span class="n">LabelEncoder</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_squared_error</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">RandomizedSearchCV</span> 
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">from</span> <span class="nn">textblob</span> <span class="kn">import</span> <span class="n">TextBlob</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">from</span> <span class="nn">pypfopt.efficient_frontier</span> <span class="kn">import</span> <span class="n">EfficientFrontier</span>
<span class="kn">from</span> <span class="nn">pypfopt</span> <span class="kn">import</span> <span class="n">risk_models</span><span class="p">,</span> <span class="n">expected_returns</span>
<span class="kn">from</span> <span class="nn">statsmodels.tsa.stattools</span> <span class="kn">import</span> <span class="n">adfuller</span>
<span class="kn">from</span> <span class="nn">tqdm</span> <span class="kn">import</span> <span class="n">tqdm</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Collecting yfinance
  Downloading yfinance-0.2.40-py2.py3-none-any.whl.metadata (11 kB)
Requirement already satisfied: pandas&gt;=1.3.0 in /home/codespace/.local/lib/python3.10/site-packages (from yfinance) (2.2.2)
Requirement already satisfied: numpy&gt;=1.16.5 in /home/codespace/.local/lib/python3.10/site-packages (from yfinance) (2.0.0)
Requirement already satisfied: requests&gt;=2.31 in /home/codespace/.local/lib/python3.10/site-packages (from yfinance) (2.32.3)
Collecting multitasking&gt;=0.0.7 (from yfinance)
  Downloading multitasking-0.0.11-py3-none-any.whl.metadata (5.5 kB)
Collecting lxml&gt;=4.9.1 (from yfinance)
  Downloading lxml-5.2.2-cp310-cp310-manylinux_2_28_x86_64.whl.metadata (3.4 kB)
Requirement already satisfied: platformdirs&gt;=2.0.0 in /home/codespace/.local/lib/python3.10/site-packages (from yfinance) (4.2.2)
Requirement already satisfied: pytz&gt;=2022.5 in /home/codespace/.local/lib/python3.10/site-packages (from yfinance) (2024.1)
Collecting frozendict&gt;=2.3.4 (from yfinance)
  Downloading frozendict-2.4.4-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (23 kB)
Collecting peewee&gt;=3.16.2 (from yfinance)
  Downloading peewee-3.17.6.tar.gz (3.0 MB)
     <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">3.0/3.0 MB</span> <span class="ansi-red-fg">22.0 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>00:0100:01
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Preparing metadata (pyproject.toml) ... done
Requirement already satisfied: beautifulsoup4&gt;=4.11.1 in /home/codespace/.local/lib/python3.10/site-packages (from yfinance) (4.12.3)
Collecting html5lib&gt;=1.1 (from yfinance)
  Downloading html5lib-1.1-py2.py3-none-any.whl.metadata (16 kB)
Requirement already satisfied: soupsieve&gt;1.2 in /home/codespace/.local/lib/python3.10/site-packages (from beautifulsoup4&gt;=4.11.1-&gt;yfinance) (2.5)
Requirement already satisfied: six&gt;=1.9 in /home/codespace/.local/lib/python3.10/site-packages (from html5lib&gt;=1.1-&gt;yfinance) (1.16.0)
Requirement already satisfied: webencodings in /home/codespace/.local/lib/python3.10/site-packages (from html5lib&gt;=1.1-&gt;yfinance) (0.5.1)
Requirement already satisfied: python-dateutil&gt;=2.8.2 in /home/codespace/.local/lib/python3.10/site-packages (from pandas&gt;=1.3.0-&gt;yfinance) (2.9.0.post0)
Requirement already satisfied: tzdata&gt;=2022.7 in /home/codespace/.local/lib/python3.10/site-packages (from pandas&gt;=1.3.0-&gt;yfinance) (2024.1)
Requirement already satisfied: charset-normalizer&lt;4,&gt;=2 in /home/codespace/.local/lib/python3.10/site-packages (from requests&gt;=2.31-&gt;yfinance) (3.3.2)
Requirement already satisfied: idna&lt;4,&gt;=2.5 in /home/codespace/.local/lib/python3.10/site-packages (from requests&gt;=2.31-&gt;yfinance) (3.7)
Requirement already satisfied: urllib3&lt;3,&gt;=1.21.1 in /usr/local/python/3.10.13/lib/python3.10/site-packages (from requests&gt;=2.31-&gt;yfinance) (2.0.7)
Requirement already satisfied: certifi&gt;=2017.4.17 in /home/codespace/.local/lib/python3.10/site-packages (from requests&gt;=2.31-&gt;yfinance) (2024.7.4)
Downloading yfinance-0.2.40-py2.py3-none-any.whl (73 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">73.5/73.5 kB</span> <span class="ansi-red-fg">1.5 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>ta <span class="ansi-cyan-fg">0:00:01</span>
Downloading frozendict-2.4.4-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (117 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">117.3/117.3 kB</span> <span class="ansi-red-fg">2.7 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>ta <span class="ansi-cyan-fg">0:00:01</span>
Downloading html5lib-1.1-py2.py3-none-any.whl (112 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">112.2/112.2 kB</span> <span class="ansi-red-fg">2.2 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>ta <span class="ansi-cyan-fg">0:00:01</span>
Downloading lxml-5.2.2-cp310-cp310-manylinux_2_28_x86_64.whl (5.0 MB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">5.0/5.0 MB</span> <span class="ansi-red-fg">36.3 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>00:0100:01
Downloading multitasking-0.0.11-py3-none-any.whl (8.5 kB)
Building wheels for collected packages: peewee
  Building wheel for peewee (pyproject.toml) ... done
  Created wheel for peewee: filename=peewee-3.17.6-cp310-cp310-linux_x86_64.whl size=854611 sha256=0b6b8ee6528965cbc34aa6099ccbfcf2eeed5343427b912b86425204077e4a05
  Stored in directory: /home/codespace/.cache/pip/wheels/4b/b9/b0/83d6e258e8f963f5ff111a2cd8c483ca59372a86e6a2535212
Successfully built peewee
Installing collected packages: peewee, multitasking, lxml, html5lib, frozendict, yfinance
<span class="ansi-yellow-fg">  WARNING: The script sample is installed in '/usr/local/python/3.10.13/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.</span><span class="ansi-yellow-fg">
</span>Successfully installed frozendict-2.4.4 html5lib-1.1 lxml-5.2.2 multitasking-0.0.11 peewee-3.17.6 yfinance-0.2.40
Note: you may need to restart the kernel to use updated packages.
Collecting yahoo_fin
  Downloading yahoo_fin-0.8.9.1-py3-none-any.whl.metadata (699 bytes)
Collecting requests-html (from yahoo_fin)
  Downloading requests_html-0.10.0-py3-none-any.whl.metadata (15 kB)
Collecting feedparser (from yahoo_fin)
  Downloading feedparser-6.0.11-py3-none-any.whl.metadata (2.4 kB)
Requirement already satisfied: requests in /home/codespace/.local/lib/python3.10/site-packages (from yahoo_fin) (2.32.3)
Requirement already satisfied: pandas in /home/codespace/.local/lib/python3.10/site-packages (from yahoo_fin) (2.2.2)
Collecting sgmllib3k (from feedparser-&gt;yahoo_fin)
  Downloading sgmllib3k-1.0.0.tar.gz (5.8 kB)
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Preparing metadata (pyproject.toml) ... done
Requirement already satisfied: numpy&gt;=1.22.4 in /home/codespace/.local/lib/python3.10/site-packages (from pandas-&gt;yahoo_fin) (2.0.0)
Requirement already satisfied: python-dateutil&gt;=2.8.2 in /home/codespace/.local/lib/python3.10/site-packages (from pandas-&gt;yahoo_fin) (2.9.0.post0)
Requirement already satisfied: pytz&gt;=2020.1 in /home/codespace/.local/lib/python3.10/site-packages (from pandas-&gt;yahoo_fin) (2024.1)
Requirement already satisfied: tzdata&gt;=2022.7 in /home/codespace/.local/lib/python3.10/site-packages (from pandas-&gt;yahoo_fin) (2024.1)
Requirement already satisfied: charset-normalizer&lt;4,&gt;=2 in /home/codespace/.local/lib/python3.10/site-packages (from requests-&gt;yahoo_fin) (3.3.2)
Requirement already satisfied: idna&lt;4,&gt;=2.5 in /home/codespace/.local/lib/python3.10/site-packages (from requests-&gt;yahoo_fin) (3.7)
Requirement already satisfied: urllib3&lt;3,&gt;=1.21.1 in /usr/local/python/3.10.13/lib/python3.10/site-packages (from requests-&gt;yahoo_fin) (2.0.7)
Requirement already satisfied: certifi&gt;=2017.4.17 in /home/codespace/.local/lib/python3.10/site-packages (from requests-&gt;yahoo_fin) (2024.7.4)
Collecting pyquery (from requests-html-&gt;yahoo_fin)
  Downloading pyquery-2.0.0-py3-none-any.whl.metadata (9.0 kB)
Collecting fake-useragent (from requests-html-&gt;yahoo_fin)
  Downloading fake_useragent-1.5.1-py3-none-any.whl.metadata (15 kB)
Collecting parse (from requests-html-&gt;yahoo_fin)
  Downloading parse-1.20.2-py2.py3-none-any.whl.metadata (22 kB)
Collecting bs4 (from requests-html-&gt;yahoo_fin)
  Downloading bs4-0.0.2-py2.py3-none-any.whl.metadata (411 bytes)
Collecting w3lib (from requests-html-&gt;yahoo_fin)
  Downloading w3lib-2.2.1-py3-none-any.whl.metadata (2.1 kB)
Collecting pyppeteer&gt;=0.0.14 (from requests-html-&gt;yahoo_fin)
  Downloading pyppeteer-2.0.0-py3-none-any.whl.metadata (7.1 kB)
Collecting appdirs&lt;2.0.0,&gt;=1.4.3 (from pyppeteer&gt;=0.0.14-&gt;requests-html-&gt;yahoo_fin)
  Downloading appdirs-1.4.4-py2.py3-none-any.whl.metadata (9.0 kB)
Collecting importlib-metadata&gt;=1.4 (from pyppeteer&gt;=0.0.14-&gt;requests-html-&gt;yahoo_fin)
  Downloading importlib_metadata-8.0.0-py3-none-any.whl.metadata (4.6 kB)
Collecting pyee&lt;12.0.0,&gt;=11.0.0 (from pyppeteer&gt;=0.0.14-&gt;requests-html-&gt;yahoo_fin)
  Downloading pyee-11.1.0-py3-none-any.whl.metadata (2.8 kB)
Collecting tqdm&lt;5.0.0,&gt;=4.42.1 (from pyppeteer&gt;=0.0.14-&gt;requests-html-&gt;yahoo_fin)
  Downloading tqdm-4.66.4-py3-none-any.whl.metadata (57 kB)
     <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">57.6/57.6 kB</span> <span class="ansi-red-fg">1.5 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>
Collecting urllib3&lt;3,&gt;=1.21.1 (from requests-&gt;yahoo_fin)
  Downloading urllib3-1.26.19-py2.py3-none-any.whl.metadata (49 kB)
     <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">49.3/49.3 kB</span> <span class="ansi-red-fg">1.1 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>ta <span class="ansi-cyan-fg">0:00:01</span>
Collecting websockets&lt;11.0,&gt;=10.0 (from pyppeteer&gt;=0.0.14-&gt;requests-html-&gt;yahoo_fin)
  Downloading websockets-10.4-cp310-cp310-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (6.4 kB)
Requirement already satisfied: six&gt;=1.5 in /home/codespace/.local/lib/python3.10/site-packages (from python-dateutil&gt;=2.8.2-&gt;pandas-&gt;yahoo_fin) (1.16.0)
Requirement already satisfied: beautifulsoup4 in /home/codespace/.local/lib/python3.10/site-packages (from bs4-&gt;requests-html-&gt;yahoo_fin) (4.12.3)
Requirement already satisfied: lxml&gt;=2.1 in /usr/local/python/3.10.13/lib/python3.10/site-packages (from pyquery-&gt;requests-html-&gt;yahoo_fin) (5.2.2)
Collecting cssselect&gt;=1.2.0 (from pyquery-&gt;requests-html-&gt;yahoo_fin)
  Downloading cssselect-1.2.0-py2.py3-none-any.whl.metadata (2.2 kB)
Collecting zipp&gt;=0.5 (from importlib-metadata&gt;=1.4-&gt;pyppeteer&gt;=0.0.14-&gt;requests-html-&gt;yahoo_fin)
  Downloading zipp-3.19.2-py3-none-any.whl.metadata (3.6 kB)
Requirement already satisfied: typing-extensions in /home/codespace/.local/lib/python3.10/site-packages (from pyee&lt;12.0.0,&gt;=11.0.0-&gt;pyppeteer&gt;=0.0.14-&gt;requests-html-&gt;yahoo_fin) (4.12.2)
Requirement already satisfied: soupsieve&gt;1.2 in /home/codespace/.local/lib/python3.10/site-packages (from beautifulsoup4-&gt;bs4-&gt;requests-html-&gt;yahoo_fin) (2.5)
Downloading yahoo_fin-0.8.9.1-py3-none-any.whl (10 kB)
Downloading feedparser-6.0.11-py3-none-any.whl (81 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">81.3/81.3 kB</span> <span class="ansi-red-fg">2.0 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>eta <span class="ansi-cyan-fg">0:00:01</span>
Downloading requests_html-0.10.0-py3-none-any.whl (13 kB)
Downloading pyppeteer-2.0.0-py3-none-any.whl (82 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">82.9/82.9 kB</span> <span class="ansi-red-fg">2.3 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>
Downloading urllib3-1.26.19-py2.py3-none-any.whl (143 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">143.9/143.9 kB</span> <span class="ansi-red-fg">3.8 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>:00:01
Downloading bs4-0.0.2-py2.py3-none-any.whl (1.2 kB)
Downloading fake_useragent-1.5.1-py3-none-any.whl (17 kB)
Downloading parse-1.20.2-py2.py3-none-any.whl (20 kB)
Downloading pyquery-2.0.0-py3-none-any.whl (22 kB)
Downloading w3lib-2.2.1-py3-none-any.whl (21 kB)
Downloading appdirs-1.4.4-py2.py3-none-any.whl (9.6 kB)
Downloading cssselect-1.2.0-py2.py3-none-any.whl (18 kB)
Downloading importlib_metadata-8.0.0-py3-none-any.whl (24 kB)
Downloading pyee-11.1.0-py3-none-any.whl (15 kB)
Downloading tqdm-4.66.4-py3-none-any.whl (78 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">78.3/78.3 kB</span> <span class="ansi-red-fg">2.1 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>
Downloading websockets-10.4-cp310-cp310-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (106 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">106.8/106.8 kB</span> <span class="ansi-red-fg">2.7 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>ta <span class="ansi-cyan-fg">0:00:01</span>
Downloading zipp-3.19.2-py3-none-any.whl (9.0 kB)
Building wheels for collected packages: sgmllib3k
  Building wheel for sgmllib3k (pyproject.toml) ... done
  Created wheel for sgmllib3k: filename=sgmllib3k-1.0.0-py3-none-any.whl size=6046 sha256=9cfba4a66f6350e71f71b5a3796e82176686342817253861ec2899f95c7d9215
  Stored in directory: /home/codespace/.cache/pip/wheels/f0/69/93/a47e9d621be168e9e33c7ce60524393c0b92ae83cf6c6e89c5
Successfully built sgmllib3k
Installing collected packages: sgmllib3k, parse, fake-useragent, appdirs, zipp, websockets, w3lib, urllib3, tqdm, pyee, feedparser, cssselect, pyquery, importlib-metadata, bs4, pyppeteer, requests-html, yahoo_fin
  Attempting uninstall: urllib3
    Found existing installation: urllib3 2.0.7
    Uninstalling urllib3-2.0.7:
      Successfully uninstalled urllib3-2.0.7
<span class="ansi-yellow-fg">  WARNING: The script tqdm is installed in '/usr/local/python/3.10.13/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.</span><span class="ansi-yellow-fg">
</span><span class="ansi-yellow-fg">  WARNING: The script pyppeteer-install is installed in '/usr/local/python/3.10.13/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.</span><span class="ansi-yellow-fg">
</span>Successfully installed appdirs-1.4.4 bs4-0.0.2 cssselect-1.2.0 fake-useragent-1.5.1 feedparser-6.0.11 importlib-metadata-8.0.0 parse-1.20.2 pyee-11.1.0 pyppeteer-2.0.0 pyquery-2.0.0 requests-html-0.10.0 sgmllib3k-1.0.0 tqdm-4.66.4 urllib3-1.26.19 w3lib-2.2.1 websockets-10.4 yahoo_fin-0.8.9.1 zipp-3.19.2
Note: you may need to restart the kernel to use updated packages.
Requirement already satisfied: scikit-learn in /home/codespace/.local/lib/python3.10/site-packages (1.5.1)
Requirement already satisfied: numpy&gt;=1.19.5 in /home/codespace/.local/lib/python3.10/site-packages (from scikit-learn) (2.0.0)
Requirement already satisfied: scipy&gt;=1.6.0 in /home/codespace/.local/lib/python3.10/site-packages (from scikit-learn) (1.14.0)
Requirement already satisfied: joblib&gt;=1.2.0 in /home/codespace/.local/lib/python3.10/site-packages (from scikit-learn) (1.4.2)
Requirement already satisfied: threadpoolctl&gt;=3.1.0 in /home/codespace/.local/lib/python3.10/site-packages (from scikit-learn) (3.5.0)
Note: you may need to restart the kernel to use updated packages.
Requirement already satisfied: matplotlib in /home/codespace/.local/lib/python3.10/site-packages (3.9.1)
Requirement already satisfied: contourpy&gt;=1.0.1 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib) (1.2.1)
Requirement already satisfied: cycler&gt;=0.10 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib) (0.12.1)
Requirement already satisfied: fonttools&gt;=4.22.0 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib) (4.53.1)
Requirement already satisfied: kiwisolver&gt;=1.3.1 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib) (1.4.5)
Requirement already satisfied: numpy&gt;=1.23 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib) (2.0.0)
Requirement already satisfied: packaging&gt;=20.0 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib) (24.1)
Requirement already satisfied: pillow&gt;=8 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib) (10.4.0)
Requirement already satisfied: pyparsing&gt;=2.3.1 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib) (3.1.2)
Requirement already satisfied: python-dateutil&gt;=2.7 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib) (2.9.0.post0)
Requirement already satisfied: six&gt;=1.5 in /home/codespace/.local/lib/python3.10/site-packages (from python-dateutil&gt;=2.7-&gt;matplotlib) (1.16.0)
Note: you may need to restart the kernel to use updated packages.
Collecting textblob
  Downloading textblob-0.18.0.post0-py3-none-any.whl.metadata (4.5 kB)
Collecting nltk&gt;=3.8 (from textblob)
  Downloading nltk-3.8.1-py3-none-any.whl.metadata (2.8 kB)
Collecting click (from nltk&gt;=3.8-&gt;textblob)
  Downloading click-8.1.7-py3-none-any.whl.metadata (3.0 kB)
Requirement already satisfied: joblib in /home/codespace/.local/lib/python3.10/site-packages (from nltk&gt;=3.8-&gt;textblob) (1.4.2)
Collecting regex&gt;=2021.8.3 (from nltk&gt;=3.8-&gt;textblob)
  Downloading regex-2024.5.15-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (40 kB)
     <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">40.9/40.9 kB</span> <span class="ansi-red-fg">1.0 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>
Requirement already satisfied: tqdm in /usr/local/python/3.10.13/lib/python3.10/site-packages (from nltk&gt;=3.8-&gt;textblob) (4.66.4)
Downloading textblob-0.18.0.post0-py3-none-any.whl (626 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">626.3/626.3 kB</span> <span class="ansi-red-fg">14.2 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>00:01
Downloading nltk-3.8.1-py3-none-any.whl (1.5 MB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">1.5/1.5 MB</span> <span class="ansi-red-fg">29.1 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>:00:01
Downloading regex-2024.5.15-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (775 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">775.1/775.1 kB</span> <span class="ansi-red-fg">17.3 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>00:01
Downloading click-8.1.7-py3-none-any.whl (97 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">97.9/97.9 kB</span> <span class="ansi-red-fg">2.5 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>eta <span class="ansi-cyan-fg">0:00:01</span>
Installing collected packages: regex, click, nltk, textblob
<span class="ansi-yellow-fg">  WARNING: The script nltk is installed in '/usr/local/python/3.10.13/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.</span><span class="ansi-yellow-fg">
</span>Successfully installed click-8.1.7 nltk-3.8.1 regex-2024.5.15 textblob-0.18.0.post0
Note: you may need to restart the kernel to use updated packages.
Requirement already satisfied: seaborn in /home/codespace/.local/lib/python3.10/site-packages (0.13.2)
Requirement already satisfied: numpy!=1.24.0,&gt;=1.20 in /home/codespace/.local/lib/python3.10/site-packages (from seaborn) (2.0.0)
Requirement already satisfied: pandas&gt;=1.2 in /home/codespace/.local/lib/python3.10/site-packages (from seaborn) (2.2.2)
Requirement already satisfied: matplotlib!=3.6.1,&gt;=3.4 in /home/codespace/.local/lib/python3.10/site-packages (from seaborn) (3.9.1)
Requirement already satisfied: contourpy&gt;=1.0.1 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib!=3.6.1,&gt;=3.4-&gt;seaborn) (1.2.1)
Requirement already satisfied: cycler&gt;=0.10 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib!=3.6.1,&gt;=3.4-&gt;seaborn) (0.12.1)
Requirement already satisfied: fonttools&gt;=4.22.0 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib!=3.6.1,&gt;=3.4-&gt;seaborn) (4.53.1)
Requirement already satisfied: kiwisolver&gt;=1.3.1 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib!=3.6.1,&gt;=3.4-&gt;seaborn) (1.4.5)
Requirement already satisfied: packaging&gt;=20.0 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib!=3.6.1,&gt;=3.4-&gt;seaborn) (24.1)
Requirement already satisfied: pillow&gt;=8 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib!=3.6.1,&gt;=3.4-&gt;seaborn) (10.4.0)
Requirement already satisfied: pyparsing&gt;=2.3.1 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib!=3.6.1,&gt;=3.4-&gt;seaborn) (3.1.2)
Requirement already satisfied: python-dateutil&gt;=2.7 in /home/codespace/.local/lib/python3.10/site-packages (from matplotlib!=3.6.1,&gt;=3.4-&gt;seaborn) (2.9.0.post0)
Requirement already satisfied: pytz&gt;=2020.1 in /home/codespace/.local/lib/python3.10/site-packages (from pandas&gt;=1.2-&gt;seaborn) (2024.1)
Requirement already satisfied: tzdata&gt;=2022.7 in /home/codespace/.local/lib/python3.10/site-packages (from pandas&gt;=1.2-&gt;seaborn) (2024.1)
Requirement already satisfied: six&gt;=1.5 in /home/codespace/.local/lib/python3.10/site-packages (from python-dateutil&gt;=2.7-&gt;matplotlib!=3.6.1,&gt;=3.4-&gt;seaborn) (1.16.0)
Note: you may need to restart the kernel to use updated packages.
Collecting PyPortfolioOpt
  Downloading pyportfolioopt-1.5.5-py3-none-any.whl.metadata (23 kB)
Collecting cvxpy&lt;2.0.0,&gt;=1.1.19 (from PyPortfolioOpt)
  Downloading cvxpy-1.5.2-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (8.9 kB)
Collecting numpy&lt;2.0.0,&gt;=1.22.4 (from PyPortfolioOpt)
  Downloading numpy-1.26.4-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (61 kB)
     <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">61.0/61.0 kB</span> <span class="ansi-red-fg">1.1 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>ta <span class="ansi-cyan-fg">0:00:01</span>
Requirement already satisfied: pandas&gt;=0.19 in /home/codespace/.local/lib/python3.10/site-packages (from PyPortfolioOpt) (2.2.2)
Requirement already satisfied: scipy&lt;2.0,&gt;=1.3 in /home/codespace/.local/lib/python3.10/site-packages (from PyPortfolioOpt) (1.14.0)
Collecting osqp&gt;=0.6.2 (from cvxpy&lt;2.0.0,&gt;=1.1.19-&gt;PyPortfolioOpt)
  Downloading osqp-0.6.7.post0-cp310-cp310-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (1.8 kB)
Collecting ecos&gt;=2 (from cvxpy&lt;2.0.0,&gt;=1.1.19-&gt;PyPortfolioOpt)
  Downloading ecos-2.0.14-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (8.0 kB)
Collecting clarabel&gt;=0.5.0 (from cvxpy&lt;2.0.0,&gt;=1.1.19-&gt;PyPortfolioOpt)
  Downloading clarabel-0.9.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (4.8 kB)
Collecting scs&gt;=3.2.4.post1 (from cvxpy&lt;2.0.0,&gt;=1.1.19-&gt;PyPortfolioOpt)
  Downloading scs-3.2.6-cp310-cp310-manylinux_2_28_x86_64.whl.metadata (2.1 kB)
Requirement already satisfied: python-dateutil&gt;=2.8.2 in /home/codespace/.local/lib/python3.10/site-packages (from pandas&gt;=0.19-&gt;PyPortfolioOpt) (2.9.0.post0)
Requirement already satisfied: pytz&gt;=2020.1 in /home/codespace/.local/lib/python3.10/site-packages (from pandas&gt;=0.19-&gt;PyPortfolioOpt) (2024.1)
Requirement already satisfied: tzdata&gt;=2022.7 in /home/codespace/.local/lib/python3.10/site-packages (from pandas&gt;=0.19-&gt;PyPortfolioOpt) (2024.1)
Collecting qdldl (from osqp&gt;=0.6.2-&gt;cvxpy&lt;2.0.0,&gt;=1.1.19-&gt;PyPortfolioOpt)
  Downloading qdldl-0.1.7.post4-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (1.7 kB)
Requirement already satisfied: six&gt;=1.5 in /home/codespace/.local/lib/python3.10/site-packages (from python-dateutil&gt;=2.8.2-&gt;pandas&gt;=0.19-&gt;PyPortfolioOpt) (1.16.0)
Downloading pyportfolioopt-1.5.5-py3-none-any.whl (61 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">61.9/61.9 kB</span> <span class="ansi-red-fg">1.7 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>
Downloading cvxpy-1.5.2-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (1.2 MB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">1.2/1.2 MB</span> <span class="ansi-red-fg">22.5 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>:00:01
Downloading numpy-1.26.4-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (18.2 MB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">18.2/18.2 MB</span> <span class="ansi-red-fg">49.2 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>:00:0100:01
Downloading clarabel-0.9.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (1.8 MB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">1.8/1.8 MB</span> <span class="ansi-red-fg">31.0 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>:00:01
Downloading ecos-2.0.14-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (218 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">218.9/218.9 kB</span> <span class="ansi-red-fg">5.0 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>:00:01
Downloading osqp-0.6.7.post0-cp310-cp310-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (297 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">297.6/297.6 kB</span> <span class="ansi-red-fg">6.4 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>:00:01
Downloading scs-3.2.6-cp310-cp310-manylinux_2_28_x86_64.whl (12.1 MB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">12.1/12.1 MB</span> <span class="ansi-red-fg">58.1 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>:00:010:01
Downloading qdldl-0.1.7.post4-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (1.1 MB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">1.1/1.1 MB</span> <span class="ansi-red-fg">22.8 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>:00:01
Installing collected packages: numpy, scs, qdldl, ecos, clarabel, osqp, cvxpy, PyPortfolioOpt
  Attempting uninstall: numpy
    Found existing installation: numpy 2.0.0
    Uninstalling numpy-2.0.0:
      Successfully uninstalled numpy-2.0.0
<span class="ansi-yellow-fg">  WARNING: The script f2py is installed in '/usr/local/python/3.10.13/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.</span><span class="ansi-yellow-fg">
</span>Successfully installed PyPortfolioOpt-1.5.5 clarabel-0.9.0 cvxpy-1.5.2 ecos-2.0.14 numpy-1.26.4 osqp-0.6.7.post0 qdldl-0.1.7.post4 scs-3.2.6
Note: you may need to restart the kernel to use updated packages.
Collecting statsmodels
  Downloading statsmodels-0.14.2-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (9.2 kB)
Requirement already satisfied: numpy&gt;=1.22.3 in /usr/local/python/3.10.13/lib/python3.10/site-packages (from statsmodels) (1.26.4)
Requirement already satisfied: scipy!=1.9.2,&gt;=1.8 in /home/codespace/.local/lib/python3.10/site-packages (from statsmodels) (1.14.0)
Requirement already satisfied: pandas!=2.1.0,&gt;=1.4 in /home/codespace/.local/lib/python3.10/site-packages (from statsmodels) (2.2.2)
Collecting patsy&gt;=0.5.6 (from statsmodels)
  Downloading patsy-0.5.6-py2.py3-none-any.whl.metadata (3.5 kB)
Requirement already satisfied: packaging&gt;=21.3 in /home/codespace/.local/lib/python3.10/site-packages (from statsmodels) (24.1)
Requirement already satisfied: python-dateutil&gt;=2.8.2 in /home/codespace/.local/lib/python3.10/site-packages (from pandas!=2.1.0,&gt;=1.4-&gt;statsmodels) (2.9.0.post0)
Requirement already satisfied: pytz&gt;=2020.1 in /home/codespace/.local/lib/python3.10/site-packages (from pandas!=2.1.0,&gt;=1.4-&gt;statsmodels) (2024.1)
Requirement already satisfied: tzdata&gt;=2022.7 in /home/codespace/.local/lib/python3.10/site-packages (from pandas!=2.1.0,&gt;=1.4-&gt;statsmodels) (2024.1)
Requirement already satisfied: six in /home/codespace/.local/lib/python3.10/site-packages (from patsy&gt;=0.5.6-&gt;statsmodels) (1.16.0)
Downloading statsmodels-0.14.2-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (10.8 MB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">10.8/10.8 MB</span> <span class="ansi-red-fg">58.3 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>:00:010:01
Downloading patsy-0.5.6-py2.py3-none-any.whl (233 kB)
   <span class="ansi-black-intense-fg">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span> <span class="ansi-green-fg">233.9/233.9 kB</span> <span class="ansi-red-fg">6.2 MB/s</span> eta <span class="ansi-cyan-fg">0:00:00</span>ta <span class="ansi-cyan-fg">0:00:01</span>
Installing collected packages: patsy, statsmodels
Successfully installed patsy-0.5.6 statsmodels-0.14.2
Note: you may need to restart the kernel to use updated packages.
Requirement already satisfied: tqdm in /usr/local/python/3.10.13/lib/python3.10/site-packages (4.66.4)
Note: you may need to restart the kernel to use updated packages.
Warning - Certain functionality 
             requires requests_html, which is not installed.
             
             Install using: 
             pip install requests_html
             
             After installation, you may have to restart your Python session.
</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Fetch the list of S&amp;P 500 companies</span>
<span class="n">tickers</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_html</span><span class="p">(</span><span class="s1">'https://en.wikipedia.org/wiki/List_of_S%26P_500_companies'</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span>
</pre></div>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Function to get live data for companies</span>
<span class="k">def</span> <span class="nf">get_live_data_for_companies</span><span class="p">(</span><span class="n">tickers</span><span class="p">):</span>
    <span class="n">live_data_for_companies</span> <span class="o">=</span> <span class="p">{}</span>
    <span class="k">for</span> <span class="n">symbol</span> <span class="ow">in</span> <span class="n">tqdm</span><span class="p">(</span><span class="n">tickers</span><span class="p">[</span><span class="s1">'Symbol'</span><span class="p">]):</span>
        <span class="k">try</span><span class="p">:</span>
            <span class="n">live_data</span> <span class="o">=</span> <span class="n">yf</span><span class="o">.</span><span class="n">Ticker</span><span class="p">(</span><span class="n">symbol</span><span class="p">)</span><span class="o">.</span><span class="n">info</span>
            <span class="n">live_data_for_companies</span><span class="p">[</span><span class="n">symbol</span><span class="p">]</span> <span class="o">=</span> <span class="n">live_data</span>
        <span class="k">except</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Could not fetch data for </span><span class="si">{</span><span class="n">symbol</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">live_data_for_companies</span>
</pre></div>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Get live data for S&amp;P 500 companies</span>
<span class="n">live_data_sp500</span> <span class="o">=</span> <span class="n">get_live_data_for_companies</span><span class="p">(</span><span class="n">tickers</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr" tabindex="0">
<pre>100%|██████████| 503/503 [00:33&lt;00:00, 15.05it/s]
</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># User input for investment details</span>
<span class="n">money</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="nb">input</span><span class="p">(</span><span class="s1">'Enter the amount of money: '</span><span class="p">))</span>
<span class="n">time</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="nb">input</span><span class="p">(</span><span class="s1">'Enter the time in weeks: '</span><span class="p">))</span>
<span class="n">risk_percentage</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="nb">input</span><span class="p">(</span><span class="s1">'Enter risk percentage (0-100): '</span><span class="p">))</span>

<span class="c1"># Validate risk percentage input</span>
<span class="k">if</span> <span class="ow">not</span> <span class="p">(</span><span class="mi">0</span> <span class="o">&lt;=</span> <span class="n">risk_percentage</span> <span class="o">&lt;=</span> <span class="mi">100</span><span class="p">):</span>
    <span class="k">raise</span> <span class="ne">ValueError</span><span class="p">(</span><span class="s1">'Invalid input for risk percentage. Please enter a value between 0 and 100.'</span><span class="p">)</span>

<span class="n">returns</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="nb">input</span><span class="p">(</span><span class="s1">'Enter returns (1-100): '</span><span class="p">))</span>

<span class="c1"># Create a DataFrame with the user input</span>
<span class="n">user_data</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">({</span>
    <span class="s1">'money'</span><span class="p">:</span> <span class="p">[</span><span class="n">money</span><span class="p">],</span>
    <span class="s1">'time'</span><span class="p">:</span> <span class="p">[</span><span class="n">time</span><span class="p">],</span>
    <span class="s1">'risk_percentage'</span><span class="p">:</span> <span class="p">[</span><span class="n">risk_percentage</span><span class="p">],</span>
    <span class="s1">'returns'</span><span class="p">:</span> <span class="p">[</span><span class="n">returns</span><span class="p">]</span>
<span class="p">})</span>

<span class="nb">print</span><span class="p">(</span><span class="s1">'</span><span class="se">\n</span><span class="s1">User Input:'</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">user_data</span><span class="p">)</span>

<span class="c1"># Prepare historical data for model training</span>
<span class="k">def</span> <span class="nf">prepare_data</span><span class="p">(</span><span class="n">tickers</span><span class="p">):</span>
    <span class="n">historical_data</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="k">for</span> <span class="n">symbol</span> <span class="ow">in</span> <span class="n">tqdm</span><span class="p">(</span><span class="n">tickers</span><span class="p">[</span><span class="s1">'Symbol'</span><span class="p">]):</span>
        <span class="k">try</span><span class="p">:</span>
            <span class="n">stock_data</span> <span class="o">=</span> <span class="n">yf</span><span class="o">.</span><span class="n">download</span><span class="p">(</span><span class="n">symbol</span><span class="p">,</span> <span class="n">period</span><span class="o">=</span><span class="s1">'3mo'</span><span class="p">)</span>
            <span class="n">stock_data</span><span class="p">[</span><span class="s1">'Symbol'</span><span class="p">]</span> <span class="o">=</span> <span class="n">symbol</span>
            <span class="n">historical_data</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">stock_data</span><span class="p">)</span>
        <span class="k">except</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Could not download data for </span><span class="si">{</span><span class="n">symbol</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">(</span><span class="n">historical_data</span><span class="p">)</span>

<span class="n">historical_data</span> <span class="o">=</span> <span class="n">prepare_data</span><span class="p">(</span><span class="n">tickers</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>
User Input:
      money  time  risk_percentage  returns
0  100000.0     2             50.0     50.0
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr" tabindex="0">
<pre>[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed

1 Failed download:
['BRK.B']: YFChartError('%ticker%: No data found, symbol may be delisted')
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed

1 Failed download:
['BF.B']: YFPricesMissingError('$%ticker%: possibly delisted; No price data found  (period=3mo)')
[*********************100%%**********************]  1 of 1 completed
 16%|█▌        | 79/503 [00:15&lt;01:01,  6.88it/s]</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>$BF.B: possibly delisted; No price data found  (period=3mo)
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr" tabindex="0">
<pre>[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed

1 Failed download:
['SW']: YFInvalidPeriodError("%ticker%: Period '3mo' is invalid, must be one of ['1d', '5d', '1mo', 'ytd', 'max']")
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
100%|██████████| 503/503 [01:33&lt;00:00,  5.40it/s]
/tmp/ipykernel_6440/164824199.py:33: FutureWarning: The behavior of array concatenation with empty entries is deprecated. In a future version, this will no longer exclude empty items when determining the result dtype. To retain the old behavior, exclude the empty entries before the concat operation.
  return pd.concat(historical_data)
</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Feature engineering</span>
<span class="n">historical_data</span><span class="p">[</span><span class="s1">'year'</span><span class="p">]</span> <span class="o">=</span> <span class="n">historical_data</span><span class="o">.</span><span class="n">index</span><span class="o">.</span><span class="n">year</span>
<span class="n">historical_data</span><span class="p">[</span><span class="s1">'month'</span><span class="p">]</span> <span class="o">=</span> <span class="n">historical_data</span><span class="o">.</span><span class="n">index</span><span class="o">.</span><span class="n">month</span>
<span class="n">historical_data</span><span class="p">[</span><span class="s1">'day'</span><span class="p">]</span> <span class="o">=</span> <span class="n">historical_data</span><span class="o">.</span><span class="n">index</span><span class="o">.</span><span class="n">day</span>
<span class="n">historical_data</span> <span class="o">=</span> <span class="n">historical_data</span><span class="o">.</span><span class="n">dropna</span><span class="p">()</span>

<span class="c1"># Label encode the stock symbols</span>
<span class="n">le</span> <span class="o">=</span> <span class="n">LabelEncoder</span><span class="p">()</span>
<span class="n">historical_data</span><span class="p">[</span><span class="s1">'symbol_encoded'</span><span class="p">]</span> <span class="o">=</span> <span class="n">le</span><span class="o">.</span><span class="n">fit_transform</span><span class="p">(</span><span class="n">historical_data</span><span class="p">[</span><span class="s1">'Symbol'</span><span class="p">])</span>

<span class="c1"># Define features and target variable</span>
<span class="n">features</span> <span class="o">=</span> <span class="n">historical_data</span><span class="p">[[</span><span class="s1">'symbol_encoded'</span><span class="p">,</span> <span class="s1">'year'</span><span class="p">,</span> <span class="s1">'month'</span><span class="p">,</span> <span class="s1">'day'</span><span class="p">,</span> <span class="s1">'Open'</span><span class="p">,</span> <span class="s1">'High'</span><span class="p">,</span> <span class="s1">'Low'</span><span class="p">,</span> <span class="s1">'Close'</span><span class="p">,</span> <span class="s1">'Volume'</span><span class="p">]]</span>
<span class="n">target</span> <span class="o">=</span> <span class="n">historical_data</span><span class="p">[</span><span class="s1">'Adj Close'</span><span class="p">]</span>

<span class="c1"># Split data into train and test sets</span>
<span class="n">X_train</span><span class="p">,</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">features</span><span class="p">,</span> <span class="n">target</span><span class="p">,</span> <span class="n">test_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">42</span><span class="p">)</span>

<span class="c1"># Use a subset of the data for hyperparameter tuning</span>
<span class="n">X_train_subset</span><span class="p">,</span> <span class="n">_</span><span class="p">,</span> <span class="n">y_train_subset</span><span class="p">,</span> <span class="n">_</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">train_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">42</span><span class="p">)</span>

<span class="c1"># Create a Random Forest Regressor</span>
<span class="n">rf_regressor</span> <span class="o">=</span> <span class="n">RandomForestRegressor</span><span class="p">()</span>

<span class="c1"># Define hyperparameters for randomized search</span>
<span class="n">param_grid</span> <span class="o">=</span> <span class="p">{</span>
    <span class="s1">'n_estimators'</span><span class="p">:</span> <span class="p">[</span><span class="mi">50</span><span class="p">,</span> <span class="mi">100</span><span class="p">,</span> <span class="mi">200</span><span class="p">],</span>
    <span class="s1">'max_depth'</span><span class="p">:</span> <span class="p">[</span><span class="kc">None</span><span class="p">,</span> <span class="mi">10</span><span class="p">,</span> <span class="mi">20</span><span class="p">],</span>
    <span class="s1">'min_samples_split'</span><span class="p">:</span> <span class="p">[</span><span class="mi">2</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">10</span><span class="p">],</span>
    <span class="s1">'min_samples_leaf'</span><span class="p">:</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
<span class="p">}</span>
</pre></div>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Perform randomized search for hyperparameter tuning</span>
<span class="n">random_search</span> <span class="o">=</span> <span class="n">RandomizedSearchCV</span><span class="p">(</span><span class="n">rf_regressor</span><span class="p">,</span> <span class="n">param_distributions</span><span class="o">=</span><span class="n">param_grid</span><span class="p">,</span> <span class="n">n_iter</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span> <span class="n">scoring</span><span class="o">=</span><span class="s1">'neg_mean_squared_error'</span><span class="p">,</span> <span class="n">n_jobs</span><span class="o">=-</span><span class="mi">1</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">42</span><span class="p">)</span>
<span class="n">random_search</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train_subset</span><span class="p">,</span> <span class="n">y_train_subset</span><span class="p">)</span>

<span class="c1"># Output the best parameters and score</span>
<span class="n">best_params</span> <span class="o">=</span> <span class="n">random_search</span><span class="o">.</span><span class="n">best_params_</span>
<span class="n">best_score</span> <span class="o">=</span> <span class="n">random_search</span><span class="o">.</span><span class="n">best_score_</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"Best Parameters: "</span><span class="p">,</span> <span class="n">best_params</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"Best Score: "</span><span class="p">,</span> <span class="n">best_score</span><span class="p">)</span>

<span class="c1"># Train the final model using the best parameters found</span>
<span class="n">final_rf_regressor</span> <span class="o">=</span> <span class="n">RandomForestRegressor</span><span class="p">(</span><span class="o">**</span><span class="n">best_params</span><span class="p">)</span>
<span class="n">final_rf_regressor</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>

<span class="c1"># Predict on the test set and calculate mean squared error</span>
<span class="n">y_pred</span> <span class="o">=</span> <span class="n">final_rf_regressor</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
<span class="n">mse</span> <span class="o">=</span> <span class="n">mean_squared_error</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">y_pred</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"Mean Squared Error on Test Set: "</span><span class="p">,</span> <span class="n">mse</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Best Parameters:  {'n_estimators': 100, 'min_samples_split': 2, 'min_samples_leaf': 1, 'max_depth': 10}
Best Score:  -33.09640191046736
Mean Squared Error on Test Set:  43.63377085655281
</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">predict_stock_investment</span><span class="p">(</span><span class="n">model</span><span class="p">,</span> <span class="n">live_data</span><span class="p">,</span> <span class="n">le</span><span class="p">):</span>
    <span class="c1"># Prepare the data for prediction</span>
    <span class="n">prepared_data</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="k">for</span> <span class="n">symbol</span><span class="p">,</span> <span class="n">data</span> <span class="ow">in</span> <span class="n">live_data</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
        <span class="k">try</span><span class="p">:</span>
            <span class="c1"># Extract the necessary features for prediction</span>
            <span class="n">prepared_data</span><span class="o">.</span><span class="n">append</span><span class="p">({</span>
                <span class="s1">'symbol'</span><span class="p">:</span> <span class="n">symbol</span><span class="p">,</span>
                <span class="s1">'Open'</span><span class="p">:</span> <span class="n">data</span><span class="p">[</span><span class="s1">'open'</span><span class="p">],</span>
                <span class="s1">'High'</span><span class="p">:</span> <span class="n">data</span><span class="p">[</span><span class="s1">'dayHigh'</span><span class="p">],</span>
                <span class="s1">'Low'</span><span class="p">:</span> <span class="n">data</span><span class="p">[</span><span class="s1">'dayLow'</span><span class="p">],</span>
                <span class="s1">'Close'</span><span class="p">:</span> <span class="n">data</span><span class="p">[</span><span class="s1">'previousClose'</span><span class="p">],</span>
                <span class="s1">'Volume'</span><span class="p">:</span> <span class="n">data</span><span class="p">[</span><span class="s1">'volume'</span><span class="p">]</span>
            <span class="p">})</span>
        <span class="k">except</span><span class="p">:</span>
            <span class="k">pass</span>
    
    <span class="c1"># Convert to DataFrame</span>
    <span class="n">prepared_df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">prepared_data</span><span class="p">)</span>
    
    <span class="c1"># Feature engineering</span>
    <span class="n">prepared_df</span><span class="p">[</span><span class="s1">'year'</span><span class="p">]</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">to_datetime</span><span class="p">(</span><span class="s1">'now'</span><span class="p">)</span><span class="o">.</span><span class="n">year</span>
    <span class="n">prepared_df</span><span class="p">[</span><span class="s1">'month'</span><span class="p">]</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">to_datetime</span><span class="p">(</span><span class="s1">'now'</span><span class="p">)</span><span class="o">.</span><span class="n">month</span>
    <span class="n">prepared_df</span><span class="p">[</span><span class="s1">'day'</span><span class="p">]</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">to_datetime</span><span class="p">(</span><span class="s1">'now'</span><span class="p">)</span><span class="o">.</span><span class="n">day</span>
    
    <span class="c1"># Label encode the stock symbols</span>
    <span class="n">prepared_df</span><span class="p">[</span><span class="s1">'symbol_encoded'</span><span class="p">]</span> <span class="o">=</span> <span class="n">le</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">prepared_df</span><span class="p">[</span><span class="s1">'symbol'</span><span class="p">])</span>
    
    <span class="c1"># Define features for prediction</span>
    <span class="n">features</span> <span class="o">=</span> <span class="n">prepared_df</span><span class="p">[[</span><span class="s1">'symbol_encoded'</span><span class="p">,</span> <span class="s1">'year'</span><span class="p">,</span> <span class="s1">'month'</span><span class="p">,</span> <span class="s1">'day'</span><span class="p">,</span> <span class="s1">'Open'</span><span class="p">,</span> <span class="s1">'High'</span><span class="p">,</span> <span class="s1">'Low'</span><span class="p">,</span> <span class="s1">'Close'</span><span class="p">,</span> <span class="s1">'Volume'</span><span class="p">]]</span>
    
    <span class="c1"># Predict returns using the model</span>
    <span class="n">predicted_returns</span> <span class="o">=</span> <span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">features</span><span class="p">)</span>
    
    <span class="c1"># Add the predicted returns to the DataFrame</span>
    <span class="n">prepared_df</span><span class="p">[</span><span class="s1">'predicted_returns'</span><span class="p">]</span> <span class="o">=</span> <span class="n">predicted_returns</span>
    
    <span class="c1"># Set symbol as index for easy access</span>
    <span class="n">prepared_df</span><span class="o">.</span><span class="n">set_index</span><span class="p">(</span><span class="s1">'symbol'</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    
    <span class="k">return</span> <span class="n">prepared_df</span><span class="p">[</span><span class="s1">'predicted_returns'</span><span class="p">]</span>

    
</pre></div>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">recommend_stocks</span><span class="p">(</span><span class="n">live_data_sp500</span><span class="p">,</span> <span class="n">predicted_returns</span><span class="p">,</span> <span class="n">risk_percentage</span><span class="p">,</span> <span class="n">money</span><span class="p">,</span> <span class="n">top_n</span><span class="o">=</span><span class="mi">5</span><span class="p">):</span>
    <span class="n">recommended_stocks</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="k">for</span> <span class="n">symbol</span><span class="p">,</span> <span class="n">data</span> <span class="ow">in</span> <span class="n">live_data_sp500</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
        <span class="k">try</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">symbol</span> <span class="ow">in</span> <span class="n">predicted_returns</span><span class="o">.</span><span class="n">index</span><span class="p">:</span>
                <span class="n">predicted_return</span> <span class="o">=</span> <span class="n">predicted_returns</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">symbol</span><span class="p">]</span>
                <span class="k">if</span> <span class="n">risk_percentage</span> <span class="o">&lt;</span> <span class="mi">33</span> <span class="ow">and</span> <span class="n">data</span><span class="p">[</span><span class="s1">'beta'</span><span class="p">]</span> <span class="o">&lt;</span> <span class="mi">1</span><span class="p">:</span>
                    <span class="n">recommended_stocks</span><span class="o">.</span><span class="n">append</span><span class="p">((</span><span class="n">symbol</span><span class="p">,</span> <span class="n">data</span><span class="p">,</span> <span class="n">predicted_return</span><span class="p">))</span>
                <span class="k">elif</span> <span class="mi">33</span> <span class="o">&lt;=</span> <span class="n">risk_percentage</span> <span class="o">&lt;</span> <span class="mi">66</span> <span class="ow">and</span> <span class="mi">1</span> <span class="o">&lt;=</span> <span class="n">data</span><span class="p">[</span><span class="s1">'beta'</span><span class="p">]</span> <span class="o">&lt;</span> <span class="mf">1.5</span><span class="p">:</span>
                    <span class="n">recommended_stocks</span><span class="o">.</span><span class="n">append</span><span class="p">((</span><span class="n">symbol</span><span class="p">,</span> <span class="n">data</span><span class="p">,</span> <span class="n">predicted_return</span><span class="p">))</span>
                <span class="k">elif</span> <span class="n">risk_percentage</span> <span class="o">&gt;=</span> <span class="mi">66</span> <span class="ow">and</span> <span class="n">data</span><span class="p">[</span><span class="s1">'beta'</span><span class="p">]</span> <span class="o">&gt;=</span> <span class="mf">1.5</span><span class="p">:</span>
                    <span class="n">recommended_stocks</span><span class="o">.</span><span class="n">append</span><span class="p">((</span><span class="n">symbol</span><span class="p">,</span> <span class="n">data</span><span class="p">,</span> <span class="n">predicted_return</span><span class="p">))</span>
        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Error processing </span><span class="si">{</span><span class="n">symbol</span><span class="si">}</span><span class="s2">: </span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
            <span class="k">pass</span>
    <span class="c1"># Sort the recommended stocks by predicted returns in descending order and select the top N</span>
    <span class="n">recommended_stocks</span><span class="o">.</span><span class="n">sort</span><span class="p">(</span><span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="n">reverse</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">recommended_stocks</span><span class="p">[:</span><span class="n">top_n</span><span class="p">]</span>
</pre></div>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.preprocessing</span> <span class="kn">import</span> <span class="n">LabelEncoder</span>

<span class="c1"># Function to refit LabelEncoder with all stock symbols</span>
<span class="k">def</span> <span class="nf">refit_label_encoder</span><span class="p">(</span><span class="n">le</span><span class="p">,</span> <span class="n">symbols</span><span class="p">):</span>
    <span class="n">le</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">symbols</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">le</span>

<span class="c1"># Refit the LabelEncoder with all possible symbols</span>
<span class="n">all_symbols</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">live_data_sp500</span><span class="o">.</span><span class="n">keys</span><span class="p">())</span>
<span class="n">le</span> <span class="o">=</span> <span class="n">refit_label_encoder</span><span class="p">(</span><span class="n">le</span><span class="p">,</span> <span class="n">all_symbols</span><span class="p">)</span>

<span class="c1"># Predict returns using the machine learning model</span>
<span class="n">predicted_returns</span> <span class="o">=</span> <span class="n">predict_stock_investment</span><span class="p">(</span><span class="n">final_rf_regressor</span><span class="p">,</span> <span class="n">live_data_sp500</span><span class="p">,</span> <span class="n">le</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">predicted_returns</span><span class="p">)</span>

<span class="c1"># Recommend stocks based on predicted returns and risk percentage</span>
<span class="n">recommended_stocks</span> <span class="o">=</span> <span class="n">recommend_stocks</span><span class="p">(</span><span class="n">live_data_sp500</span><span class="p">,</span> <span class="n">predicted_returns</span><span class="p">,</span> <span class="n">risk_percentage</span><span class="p">,</span> <span class="n">money</span><span class="p">,</span> <span class="n">top_n</span><span class="o">=</span><span class="mi">6</span><span class="p">)</span>

<span class="c1"># Print recommended stocks and reasons for selection</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'</span><span class="se">\n</span><span class="s1">Recommended Stocks:'</span><span class="p">)</span>
<span class="k">for</span> <span class="n">symbol</span><span class="p">,</span> <span class="n">data</span><span class="p">,</span> <span class="n">returns</span> <span class="ow">in</span> <span class="n">recommended_stocks</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"</span><span class="se">\n</span><span class="s2">Symbol: </span><span class="si">{</span><span class="n">symbol</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Company: </span><span class="si">{</span><span class="n">data</span><span class="p">[</span><span class="s1">'longName'</span><span class="p">]</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Volatility (A Value of 1.5 means the stock is 50% more volatile than the broader market): </span><span class="si">{</span><span class="n">data</span><span class="p">[</span><span class="s1">'beta'</span><span class="p">]</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Market Cap: </span><span class="si">{</span><span class="n">data</span><span class="p">[</span><span class="s1">'marketCap'</span><span class="p">]</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Industry: </span><span class="si">{</span><span class="n">data</span><span class="p">[</span><span class="s1">'industry'</span><span class="p">]</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Predicted Returns: </span><span class="si">{</span><span class="n">returns</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Reason: </span><span class="si">{</span><span class="s1">'Low risk'</span><span class="w"> </span><span class="k">if</span><span class="w"> </span><span class="n">risk_percentage</span><span class="w"> </span><span class="o">&lt;</span><span class="w"> </span><span class="mi">33</span><span class="w"> </span><span class="k">else</span><span class="w"> </span><span class="s1">'Medium risk'</span><span class="w"> </span><span class="k">if</span><span class="w"> </span><span class="n">risk_percentage</span><span class="w"> </span><span class="o">&lt;</span><span class="w"> </span><span class="mi">66</span><span class="w"> </span><span class="k">else</span><span class="w"> </span><span class="s1">'High risk'</span><span class="si">}</span><span class="s2"> stock with appropriate beta value."</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>symbol
MMM     103.018002
AOS      85.902451
ABT     103.992902
ABBV    169.420488
ACN     297.326778
           ...    
XYL     137.771458
YUM     129.158394
ZBRA    327.991143
ZBH     108.063866
ZTS     177.565833
Name: predicted_returns, Length: 501, dtype: float64
Error processing GEHC: 'beta'
Error processing GEV: 'beta'
Error processing KVUE: 'beta'
Error processing SOLV: 'beta'
Error processing VLTO: 'beta'

Recommended Stocks:

Symbol: NVR
Company: NVR, Inc.
Volatility (A Value of 1.5 means the stock is 50% more volatile than the broader market): 1.168
Market Cap: 25254012928
Industry: Residential Construction
Predicted Returns: 8016.433032226562
Reason: Medium risk stock with appropriate beta value.

Symbol: BKNG
Company: Booking Holdings Inc.
Volatility (A Value of 1.5 means the stock is 50% more volatile than the broader market): 1.385
Market Cap: 136606703616
Industry: Travel Services
Predicted Returns: 3944.89720703125
Reason: Medium risk stock with appropriate beta value.

Symbol: FICO
Company: Fair Isaac Corporation
Volatility (A Value of 1.5 means the stock is 50% more volatile than the broader market): 1.336
Market Cap: 39253757952
Industry: Software - Application
Predicted Returns: 1575.3682165527343
Reason: Medium risk stock with appropriate beta value.

Symbol: AVGO
Company: Broadcom Inc.
Volatility (A Value of 1.5 means the stock is 50% more volatile than the broader market): 1.188
Market Cap: 7916414304256
Industry: Semiconductors
Predicted Returns: 1573.2097485351562
Reason: Medium risk stock with appropriate beta value.

Symbol: MTD
Company: Mettler-Toledo International Inc.
Volatility (A Value of 1.5 means the stock is 50% more volatile than the broader market): 1.167
Market Cap: 29029191680
Industry: Diagnostics &amp; Research
Predicted Returns: 1358.3685296659924
Reason: Medium risk stock with appropriate beta value.

Symbol: TDG
Company: TransDigm Group Incorporated
Volatility (A Value of 1.5 means the stock is 50% more volatile than the broader market): 1.382
Market Cap: 69517803520
Industry: Aerospace &amp; Defense
Predicted Returns: 1253.9945891103487
Reason: Medium risk stock with appropriate beta value.
</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Function to fetch news articles for recommended stocks</span>
<span class="k">def</span> <span class="nf">fetch_news_articles</span><span class="p">(</span><span class="n">symbol</span><span class="p">):</span>
    <span class="k">try</span><span class="p">:</span>
        <span class="n">ticker</span> <span class="o">=</span> <span class="n">yf</span><span class="o">.</span><span class="n">Ticker</span><span class="p">(</span><span class="n">symbol</span><span class="p">)</span>
        <span class="n">news</span> <span class="o">=</span> <span class="n">ticker</span><span class="o">.</span><span class="n">news</span>
        <span class="k">if</span> <span class="ow">not</span> <span class="n">news</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"No news articles found for </span><span class="si">{</span><span class="n">symbol</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
        <span class="k">return</span> <span class="n">news</span><span class="p">[:</span><span class="mi">5</span><span class="p">]</span>  <span class="c1"># Return the top 5 news articles</span>
    <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Error fetching news for </span><span class="si">{</span><span class="n">symbol</span><span class="si">}</span><span class="s2">: </span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
        <span class="k">return</span> <span class="p">[]</span>
</pre></div>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Fetch news articles for recommended stocks</span>
<span class="k">for</span> <span class="n">stock</span><span class="p">,</span> <span class="n">data</span><span class="p">,</span> <span class="n">returns</span> <span class="ow">in</span> <span class="n">recommended_stocks</span><span class="p">:</span>
    <span class="n">news_articles</span> <span class="o">=</span> <span class="n">fetch_news_articles</span><span class="p">(</span><span class="n">stock</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s1">'</span><span class="se">\n</span><span class="s1">News for </span><span class="si">{</span><span class="n">stock</span><span class="si">}</span><span class="s1">:'</span><span class="p">)</span>
    <span class="k">if</span> <span class="n">news_articles</span><span class="p">:</span>
        <span class="k">for</span> <span class="n">article</span> <span class="ow">in</span> <span class="n">news_articles</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Title: </span><span class="si">{</span><span class="n">article</span><span class="p">[</span><span class="s1">'title'</span><span class="p">]</span><span class="si">}</span><span class="se">\n</span><span class="s2">Link: </span><span class="si">{</span><span class="n">article</span><span class="p">[</span><span class="s1">'link'</span><span class="p">]</span><span class="si">}</span><span class="se">\n</span><span class="s2">"</span><span class="p">)</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">"No news articles found."</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>
News for NVR:
Title: Q1 Earnings Highs And Lows: NVR (NYSE:NVR) Vs The Rest Of The Home Builders Stocks
Link: https://finance.yahoo.com/news/q1-earnings-highs-lows-nvr-080555820.html

Title: NVR's (NYSE:NVR) investors will be pleased with their impressive 126% return over the last five years
Link: https://finance.yahoo.com/news/nvrs-nyse-nvr-investors-pleased-140340110.html

Title: Why Opendoor, Home Depot, and NVR, Inc. Rallied Today
Link: https://finance.yahoo.com/m/36578165-4a56-32de-ba2c-af979d84fa3e/why-opendoor%2C-home-depot%2C-and.html

Title: 3 Companies That Should Consider a 10-for-1 Stock Split
Link: https://finance.yahoo.com/news/3-companies-consider-10-1-100000428.html

Title: Here's Why NVR (NVR) is a Strong Momentum Stock
Link: https://finance.yahoo.com/news/heres-why-nvr-nvr-strong-135011043.html


News for BKNG:
Title: Booking Holdings Shares Rise After Upgrade From Benchmark
Link: https://finance.yahoo.com/news/booking-holdings-shares-rise-upgrade-185950498.html

Title: Booking Holdings Is a Growth Story. The Case for Buying Now.
Link: https://finance.yahoo.com/m/ea64515c-823d-33ad-b2c3-d0a0e58bd3f7/booking-holdings-is-a-growth.html

Title: Tesla downgraded, Booking Holdings upgraded: Wall Street's top analyst calls
Link: https://finance.yahoo.com/news/tesla-downgraded-booking-holdings-upgraded-134246270.html

Title: Wall Street Analysts See Booking Holdings (BKNG) as a Buy: Should You Invest?
Link: https://finance.yahoo.com/news/wall-street-analysts-see-booking-133010099.html

Title: Growing India Travel Market Helps This IBD 50 Stock Book 80% Gains This Year
Link: https://finance.yahoo.com/m/ee1eb8bc-e666-3221-b3dc-9432c0d915b0/growing-india-travel-market.html


News for FICO:
Title: Beat the Market Like Zacks: Carvana, Adobe, Amgen in Focus
Link: https://finance.yahoo.com/news/beat-market-zacks-carvana-adobe-120100753.html

Title: 3 Stocks that Should Follow Nvidia and Go for the Split
Link: https://finance.yahoo.com/news/3-stocks-nvidia-split-141325604.html

Title: Fair Isaac (FICO) Rides on Solid Portfolio, Expanding Clientele
Link: https://finance.yahoo.com/news/fair-isaac-fico-rides-solid-144700737.html

Title: Goldman Sachs Adjusts Price Target on Fair Isaac to $1,652 From $1,502, Maintains Buy Rating
Link: https://finance.yahoo.com/news/goldman-sachs-adjusts-price-target-095859999.html

Title: FICO Appoints EVP Nikhil Behl to Lead Software Business
Link: https://finance.yahoo.com/news/fico-appoints-evp-nikhil-behl-123000982.html


News for AVGO:
Title: Is Broadcom a Better Stock-Split Buy Than Nvidia? Wall Street Thinks So.
Link: https://finance.yahoo.com/m/1327ceb0-7d81-33f0-a464-38c0e95bf988/is-broadcom-a-better.html

Title: Where Will Broadcom Stock Be in 10 Years?
Link: https://finance.yahoo.com/m/3c819817-e428-3125-870e-1160e1de9477/where-will-broadcom-stock-be.html

Title: Correlations Between Credit and Equities Are Breaking Down
Link: https://finance.yahoo.com/news/correlations-between-credit-equities-breaking-190000478.html

Title: Will Broadcom Stock Soar After Its 10-for-1 Stock Split? Here's What History Shows.
Link: https://finance.yahoo.com/m/7b5863a2-93ce-3692-8407-3021e5b06a37/will-broadcom-stock-soar.html

Title: This investment fad looks good, but the math says you should probably avoid it
Link: https://finance.yahoo.com/m/5cc523d6-8ecc-38da-b5f8-6406f0dc7c6d/this-investment-fad-looks.html


News for MTD:
Title: Goldman Sachs Adjusts Price Target on Mettler-Toledo International to $1,300 From $1,150, Maintains Neutral Rating
Link: https://finance.yahoo.com/news/goldman-sachs-adjusts-price-target-105812869.html

Title: Mettler-Toledo International Inc. to Host Second Quarter 2024 Earnings Conference Call
Link: https://finance.yahoo.com/news/mettler-toledo-international-inc-host-203000956.html

Title: 7 High Priced Stocks That Would Benefit From a Stock Split
Link: https://finance.yahoo.com/news/7-high-priced-stocks-benefit-194511028.html

Title: Mettler-Toledo International's (NYSE:MTD) five-year total shareholder returns outpace the underlying earnings growth
Link: https://finance.yahoo.com/news/mettler-toledo-internationals-nyse-mtd-154456469.html

Title: Evercore ISI Adjusts Price Target on Mettler-Toledo International to $1,390 From $1,375, Maintains In-line Rating
Link: https://finance.yahoo.com/news/evercore-isi-adjusts-price-target-115849338.html

</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">plot_predicted_returns</span><span class="p">(</span><span class="n">recommended_stocks</span><span class="p">,</span> <span class="n">model</span><span class="p">,</span> <span class="n">live_data_sp500</span><span class="p">,</span> <span class="n">le</span><span class="p">):</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">14</span><span class="p">,</span> <span class="mi">7</span><span class="p">))</span>
    <span class="n">plotted</span> <span class="o">=</span> <span class="kc">False</span>  <span class="c1"># Track if any data has been successfully plotted</span>
    <span class="k">for</span> <span class="n">symbol</span><span class="p">,</span> <span class="n">data</span><span class="p">,</span> <span class="n">returns</span> <span class="ow">in</span> <span class="n">recommended_stocks</span><span class="p">:</span>
        <span class="k">try</span><span class="p">:</span>
            <span class="c1"># Check if symbol exists in live_data_sp500 and has necessary columns</span>
            <span class="k">if</span> <span class="n">symbol</span> <span class="ow">in</span> <span class="n">live_data_sp500</span> <span class="ow">and</span> <span class="nb">all</span><span class="p">(</span><span class="n">col</span> <span class="ow">in</span> <span class="n">live_data_sp500</span><span class="p">[</span><span class="n">symbol</span><span class="p">]</span> <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">'Close'</span><span class="p">,</span> <span class="s1">'High'</span><span class="p">,</span> <span class="s1">'Low'</span><span class="p">,</span> <span class="s1">'Open'</span><span class="p">,</span> <span class="s1">'Volume'</span><span class="p">]):</span>
                <span class="c1"># Prepare input data for prediction using live market data</span>
                <span class="n">input_data</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">([</span><span class="n">live_data_sp500</span><span class="p">[</span><span class="n">symbol</span><span class="p">]])</span>  <span class="c1"># Convert dictionary to DataFrame</span>
                <span class="n">input_data</span> <span class="o">=</span> <span class="n">input_data</span><span class="p">[[</span><span class="s1">'Close'</span><span class="p">,</span> <span class="s1">'High'</span><span class="p">,</span> <span class="s1">'Low'</span><span class="p">,</span> <span class="s1">'Open'</span><span class="p">,</span> <span class="s1">'Volume'</span><span class="p">]]</span>  <span class="c1"># Select necessary columns</span>

                <span class="c1"># Predict returns using the model</span>
                <span class="n">predicted_returns</span> <span class="o">=</span> <span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">input_data</span><span class="p">)</span>

                <span class="c1"># Plotting</span>
                <span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">symbol</span><span class="p">,</span> <span class="n">predicted_returns</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">symbol</span><span class="p">)</span>
                <span class="n">plotted</span> <span class="o">=</span> <span class="kc">True</span>

            <span class="k">else</span><span class="p">:</span>
                <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Skipping symbol </span><span class="si">{</span><span class="n">symbol</span><span class="si">}</span><span class="s2">: Missing required columns"</span><span class="p">)</span>

        <span class="k">except</span> <span class="ne">KeyError</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Error processing symbol </span><span class="si">{</span><span class="n">symbol</span><span class="si">}</span><span class="s2">: </span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>

    <span class="k">if</span> <span class="n">plotted</span><span class="p">:</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">'Stock Symbol'</span><span class="p">)</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">'Predicted Returns'</span><span class="p">)</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">'Predicted Returns for Recommended Stocks'</span><span class="p">)</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">rotation</span><span class="o">=</span><span class="mi">45</span><span class="p">)</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">()</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">tight_layout</span><span class="p">()</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">"No data available to plot."</span><span class="p">)</span>

<span class="c1"># Example usage</span>
<span class="n">plot_predicted_returns</span><span class="p">(</span><span class="n">recommended_stocks</span><span class="p">,</span> <span class="n">final_rf_regressor</span><span class="p">,</span> <span class="n">live_data_sp500</span><span class="p">,</span> <span class="n">le</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Skipping symbol NVR: Missing required columns
Skipping symbol BKNG: Missing required columns
Skipping symbol FICO: Missing required columns
Skipping symbol AVGO: Missing required columns
Skipping symbol MTD: Missing required columns
No data available to plot.
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>&lt;Figure size 1400x700 with 0 Axes&gt;</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">calculate_sharpe_ratio</span><span class="p">(</span><span class="n">recommended_stocks</span><span class="p">,</span> <span class="n">risk_free_rate</span><span class="o">=</span><span class="mf">0.02</span><span class="p">):</span>
    <span class="n">sharpe_ratios</span> <span class="o">=</span> <span class="p">{}</span>
    <span class="k">for</span> <span class="n">symbol</span><span class="p">,</span> <span class="n">data</span><span class="p">,</span> <span class="n">returns</span> <span class="ow">in</span> <span class="n">recommended_stocks</span><span class="p">:</span>
        <span class="n">daily_returns</span> <span class="o">=</span> <span class="n">returns</span>  <span class="c1"># Replace with actual daily returns calculation if available</span>
        
        <span class="k">if</span> <span class="n">np</span><span class="o">.</span><span class="n">std</span><span class="p">(</span><span class="n">daily_returns</span><span class="p">)</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Skipping </span><span class="si">{</span><span class="n">symbol</span><span class="si">}</span><span class="s2"> due to zero variability in returns."</span><span class="p">)</span>
            <span class="k">continue</span>
        
        <span class="n">avg_return</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">daily_returns</span><span class="p">)</span>
        <span class="n">std_return</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">std</span><span class="p">(</span><span class="n">daily_returns</span><span class="p">)</span>
        
        <span class="n">sharpe_ratio</span> <span class="o">=</span> <span class="p">(</span><span class="n">avg_return</span> <span class="o">-</span> <span class="n">risk_free_rate</span><span class="p">)</span> <span class="o">/</span> <span class="n">std_return</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="mi">252</span><span class="p">)</span>
        
        <span class="n">sharpe_ratios</span><span class="p">[</span><span class="n">symbol</span><span class="p">]</span> <span class="o">=</span> <span class="n">sharpe_ratio</span>
    
    <span class="k">return</span> <span class="n">sharpe_ratios</span>

<span class="c1"># Calculate and print Sharpe ratios with handling for zero variability</span>
<span class="n">sharpe_ratios</span> <span class="o">=</span> <span class="n">calculate_sharpe_ratio</span><span class="p">(</span><span class="n">recommended_stocks</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'</span><span class="se">\n</span><span class="s1">Sharpe Ratios:'</span><span class="p">)</span>
<span class="k">for</span> <span class="n">symbol</span><span class="p">,</span> <span class="n">ratio</span> <span class="ow">in</span> <span class="n">sharpe_ratios</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"</span><span class="si">{</span><span class="n">symbol</span><span class="si">}</span><span class="s2">: </span><span class="si">{</span><span class="n">ratio</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Skipping NVR due to zero variability in returns.
Skipping BKNG due to zero variability in returns.
Skipping FICO due to zero variability in returns.
Skipping AVGO due to zero variability in returns.
Skipping MTD due to zero variability in returns.

Sharpe Ratios:
</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Sentiment analysis of news articles for recommended stocks</span>
<span class="k">def</span> <span class="nf">sentiment_analysis</span><span class="p">(</span><span class="n">news_articles</span><span class="p">):</span>
    <span class="n">sentiments</span> <span class="o">=</span> <span class="p">{}</span>
    <span class="k">for</span> <span class="n">article</span> <span class="ow">in</span> <span class="n">news_articles</span><span class="p">:</span>
        <span class="n">analysis</span> <span class="o">=</span> <span class="n">TextBlob</span><span class="p">(</span><span class="n">article</span><span class="p">[</span><span class="s1">'title'</span><span class="p">])</span>
        <span class="n">sentiments</span><span class="p">[</span><span class="n">article</span><span class="p">[</span><span class="s1">'title'</span><span class="p">]]</span> <span class="o">=</span> <span class="n">analysis</span><span class="o">.</span><span class="n">sentiment</span><span class="o">.</span><span class="n">polarity</span>
    <span class="k">return</span> <span class="n">sentiments</span>

<span class="c1"># Perform sentiment analysis and print results</span>
<span class="k">for</span> <span class="n">stock</span><span class="p">,</span> <span class="n">_</span><span class="p">,</span> <span class="n">_</span> <span class="ow">in</span> <span class="n">recommended_stocks</span><span class="p">:</span>  <span class="c1"># Unpack all three values, ignoring the last two</span>
    <span class="n">news_articles</span> <span class="o">=</span> <span class="n">fetch_news_articles</span><span class="p">(</span><span class="n">stock</span><span class="p">)</span>
    <span class="n">sentiments</span> <span class="o">=</span> <span class="n">sentiment_analysis</span><span class="p">(</span><span class="n">news_articles</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s1">'</span><span class="se">\n</span><span class="s1">Sentiment Analysis for </span><span class="si">{</span><span class="n">stock</span><span class="si">}</span><span class="s1">:'</span><span class="p">)</span>
    <span class="k">for</span> <span class="n">title</span><span class="p">,</span> <span class="n">sentiment</span> <span class="ow">in</span> <span class="n">sentiments</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
        <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"Title: </span><span class="si">{</span><span class="n">title</span><span class="si">}</span><span class="se">\n</span><span class="s2">Sentiment Polarity: </span><span class="si">{</span><span class="n">sentiment</span><span class="si">}</span><span class="se">\n</span><span class="s2">"</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>
Sentiment Analysis for NVR:
Title: Q1 Earnings Highs And Lows: NVR (NYSE:NVR) Vs The Rest Of The Home Builders Stocks
Sentiment Polarity: 0.0

Title: NVR's (NYSE:NVR) investors will be pleased with their impressive 126% return over the last five years
Sentiment Polarity: 0.5

Title: Why Opendoor, Home Depot, and NVR, Inc. Rallied Today
Sentiment Polarity: 0.0

Title: 3 Companies That Should Consider a 10-for-1 Stock Split
Sentiment Polarity: 0.0

Title: Here's Why NVR (NVR) is a Strong Momentum Stock
Sentiment Polarity: 0.4333333333333333


Sentiment Analysis for BKNG:
Title: Booking Holdings Shares Rise After Upgrade From Benchmark
Sentiment Polarity: 0.0

Title: Booking Holdings Is a Growth Story. The Case for Buying Now.
Sentiment Polarity: 0.0

Title: Tesla downgraded, Booking Holdings upgraded: Wall Street's top analyst calls
Sentiment Polarity: 0.5

Title: Wall Street Analysts See Booking Holdings (BKNG) as a Buy: Should You Invest?
Sentiment Polarity: 0.0

Title: Growing India Travel Market Helps This IBD 50 Stock Book 80% Gains This Year
Sentiment Polarity: 0.0


Sentiment Analysis for FICO:
Title: Beat the Market Like Zacks: Carvana, Adobe, Amgen in Focus
Sentiment Polarity: 0.0

Title: 3 Stocks that Should Follow Nvidia and Go for the Split
Sentiment Polarity: 0.0

Title: Fair Isaac (FICO) Rides on Solid Portfolio, Expanding Clientele
Sentiment Polarity: 0.35

Title: Goldman Sachs Adjusts Price Target on Fair Isaac to $1,652 From $1,502, Maintains Buy Rating
Sentiment Polarity: 0.7

Title: FICO Appoints EVP Nikhil Behl to Lead Software Business
Sentiment Polarity: 0.0


Sentiment Analysis for AVGO:
Title: Is Broadcom a Better Stock-Split Buy Than Nvidia? Wall Street Thinks So.
Sentiment Polarity: 0.5

Title: Where Will Broadcom Stock Be in 10 Years?
Sentiment Polarity: 0.0

Title: Correlations Between Credit and Equities Are Breaking Down
Sentiment Polarity: -0.15555555555555559

Title: Will Broadcom Stock Soar After Its 10-for-1 Stock Split? Here's What History Shows.
Sentiment Polarity: 0.0

Title: This investment fad looks good, but the math says you should probably avoid it
Sentiment Polarity: 0.7


Sentiment Analysis for MTD:
Title: Goldman Sachs Adjusts Price Target on Mettler-Toledo International to $1,300 From $1,150, Maintains Neutral Rating
Sentiment Polarity: 0.0

Title: Mettler-Toledo International Inc. to Host Second Quarter 2024 Earnings Conference Call
Sentiment Polarity: 0.0

Title: 7 High Priced Stocks That Would Benefit From a Stock Split
Sentiment Polarity: 0.16

Title: Mettler-Toledo International's (NYSE:MTD) five-year total shareholder returns outpace the underlying earnings growth
Sentiment Polarity: 0.0

Title: Evercore ISI Adjusts Price Target on Mettler-Toledo International to $1,390 From $1,375, Maintains In-line Rating
Sentiment Polarity: 0.0

</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">monte_carlo_simulation</span><span class="p">(</span><span class="n">recommended_stocks</span><span class="p">,</span> <span class="n">num_simulations</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">time_horizon</span><span class="o">=</span><span class="mi">252</span><span class="p">):</span>
    <span class="n">simulated_portfolios</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="k">for</span> <span class="n">symbol</span><span class="p">,</span> <span class="n">_</span><span class="p">,</span> <span class="n">_</span> <span class="ow">in</span> <span class="n">recommended_stocks</span><span class="p">:</span> <span class="c1"># Unpack into three variables to handle the structure of recommended_stocks</span>
        <span class="n">historical_prices</span> <span class="o">=</span> <span class="n">yf</span><span class="o">.</span><span class="n">download</span><span class="p">(</span><span class="n">symbol</span><span class="p">,</span> <span class="n">period</span><span class="o">=</span><span class="s1">'3mo'</span><span class="p">)[</span><span class="s1">'Adj Close'</span><span class="p">]</span>
        <span class="n">returns</span> <span class="o">=</span> <span class="n">historical_prices</span><span class="o">.</span><span class="n">pct_change</span><span class="p">()</span><span class="o">.</span><span class="n">dropna</span><span class="p">()</span>
        <span class="n">avg_return</span> <span class="o">=</span> <span class="n">returns</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
        <span class="n">std_dev</span> <span class="o">=</span> <span class="n">returns</span><span class="o">.</span><span class="n">std</span><span class="p">()</span>
        
        <span class="k">for</span> <span class="n">_</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">num_simulations</span><span class="p">):</span>
            <span class="n">simulation</span> <span class="o">=</span> <span class="p">[</span><span class="n">historical_prices</span><span class="o">.</span><span class="n">iloc</span><span class="p">[</span><span class="o">-</span><span class="mi">1</span><span class="p">]]</span>
            <span class="k">for</span> <span class="n">_</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">time_horizon</span><span class="p">):</span>
                <span class="n">next_price</span> <span class="o">=</span> <span class="n">simulation</span><span class="p">[</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span> <span class="o">*</span> <span class="p">(</span><span class="mi">1</span> <span class="o">+</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">normal</span><span class="p">(</span><span class="n">avg_return</span><span class="p">,</span> <span class="n">std_dev</span><span class="p">))</span>
                <span class="n">simulation</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">next_price</span><span class="p">)</span>
            <span class="n">simulated_portfolios</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">simulation</span><span class="p">)</span>
    
    <span class="k">return</span> <span class="n">simulated_portfolios</span>

<span class="c1"># Perform Monte Carlo simulation and plot results</span>
<span class="n">simulated_portfolios</span> <span class="o">=</span> <span class="n">monte_carlo_simulation</span><span class="p">(</span><span class="n">recommended_stocks</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">14</span><span class="p">,</span> <span class="mi">7</span><span class="p">))</span>
<span class="k">for</span> <span class="n">portfolio</span> <span class="ow">in</span> <span class="n">simulated_portfolios</span><span class="p">:</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">portfolio</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">'red'</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">'Monte Carlo Simulation of Portfolio'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">'Time (days)'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">'Portfolio Value'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr" tabindex="0">
<pre>[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
[*********************100%%**********************]  1 of 1 completed
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABJEAAAJwCAYAAAA5hvCvAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjkuMSwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy/TGe4hAAAACXBIWXMAAA9hAAAPYQGoP6dpAADzYklEQVR4nOzdeZhkZXk+/vvUvldv0zNMIMMaBERRSXRExWUisqqgBpUACQLqIEHURPSnYBRRcGFRURIDxC0uMS6gIiJiBCR83ZVFUBAXZqa3qural3N+fzw+/Z6qruqu6q7u6qq6P9dVV3dX13JqPefc53mf13IcxwEREREREREREdESPL1eACIiIiIiIiIi2vgYIhERERERERER0bIYIhERERERERER0bIYIhERERERERER0bIYIhERERERERER0bIYIhERERERERER0bIYIhERERERERER0bIYIhERERERERER0bIYIhERERERERER0bIYIhEREVHf2XfffXHmmWeu+/3ecMMNsCwLjz766LrfNwBYloVLLrmkq7f53Oc+F8997nO7epvdtnv3brzsZS/D+Pg4LMvClVde2etFWlI2m8VrXvMabNmyBZZl4YILLujo+o2vc6/fd0RERIohEhER0RrSnT/LsvCDH/xg0f8dx8E+++wDy7JwwgknrOmy3HXXXbjkkkuQSqXW5PZ/85vf4Nxzz8X++++PUCiERCKBo446CldddRUKhcKa3Ge3lMtlXHXVVXjKU56CRCKBkZERHHbYYTjnnHPwwAMP9HrxVu2+++7DJZdc0rchxBvf+EbccsstuOiii/CpT30KL3rRi1peVj9vlmXB4/Fg69ateOELX4jvfe97XV2mb3zjGy0Dvfe+97244YYb8LrXvQ6f+tSn8Pd///ddvW8iIqJe8fV6AYiIiIZBKBTCZz/7WTzrWc+qO/+OO+7AH/7wBwSDwTVfhrvuugvvete7cOaZZ2JkZKSrt33zzTfj5S9/OYLBIE4//XQ88YlPRLlcxg9+8AO85S1vwa9+9Stcd911Xb3PbjrllFPwzW9+E6985Stx9tlno1Kp4IEHHsBNN92EZz7zmXjCE54AAPj7v/97nHrqqevyenXTfffdh3e961147nOfi3333bfuf9/+9rd7s1Ad+O53v4sXv/jFePOb39zW5f/2b/8Wp59+OhzHwSOPPIKP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XHS/re7/yiuvdAA4n/70pxfOK5fLzvbt251YLOZkMhnHcRznkUcecQA44+Pjzuzs7MJlv/rVrzoAnK9//euL7sutk9cMgLNz584lb8992bPOOsuZmppy9uzZ49xzzz3OC17wAgeA88EPftBxHMc54ogjnMnJSWdmZmbhej/72c8cj8fjnH766QvnXXzxxQ4A55WvfOWi+9m5c6fTalO68fPsOO0/r/oY3K9z4/tuz549TiAQcF74whfWPU8f+chHHADOf/zHf7TxTBEREXWOw9mIiIjWySte8QoUCgXcdNNNmJ+fx0033dRyKNs3vvENeL1enH/++XXnv+lNb4LjOPjmN79Zd/6OHTtwwAEHLPz9pCc9CYlEAr/97W+XXa4vf/nLsG0br3jFKzA9Pb1w2rJlCw466CDcfvvtLa+byWQAAPF4fNn7Ue6eRul0GtPT0zj66KPx29/+Ful0uu6y++23H4455phlb/Mb3/gG/uZv/qaucXksFsM555yDRx99FPfdd1/L61qWhVtuuQXvec97MDo6is997nPYuXMntm3bhr/7u79ra3jQoYceiu3bty/8/fSnPx0A8PznPx9/+Zd/uej8dl6Xdrify0qlgpmZGRx44IEYGRnBj3/84xXd5je+8Q1s2bIFr3zlKxfO8/v9OP/885HNZnHHHXfUXf7v/u7vMDo6uvD3s5/9bADLP8bVvGbL+eQnP4lNmzZhcnIST3/603HnnXfiwgsvxAUXXIDHH38cP/3pT3HmmWdibGxs4TpPetKT8Ld/+7f4xje+sej2Xvva1654WVSnz+tSvvOd76BcLuOCCy6oq2g7++yzkUgkutKDjIiIqBkOZyMiIlonmzZtwo4dO/DZz34W+XwetVoNL3vZy5pe9ne/+x22bt26KJzRIUi/+93v6s53BxVqdHQUc3Nzyy7XQw89BMdxcNBBBzX9/1LDYhKJBABgfn5+2ftRd955Jy6++GLcfffdyOfzdf9Lp9NIJpMLf++3335t3ebvfve7hYDGzf18PfGJT2x5/WAwiLe//e14+9vfjscffxx33HEHrrrqKnzhC1+A3+/Hpz/96SXvv/H518ewzz77ND2/ndelHYVCAZdddhmuv/56/PGPf6zrl9UYyLXrd7/7HQ466KBFw+3afe9poLTcY1zta7aUF7/4xTjvvPNgWRbi8TgOO+ywhWbYuvzNhkYecsghuOWWWxY1z273fbiUTp/X5W4LWPwYAoEA9t9//45ui4iIqBMMkYiIiNbRq171Kpx99tnYtWsXjj322I5mnFpKq5mbnIYm3M3Ytg3LsvDNb36z6e3EYrGW100kEti6dSt++ctftrWcv/nNb/CCF7wAT3jCE/ChD30I++yzDwKBAL7xjW/gwx/+MGzbrrt8t2dia8dee+2FU089FaeccgoOO+wwfOELX8ANN9ywZK+kVs9/O6+LNo5uVKvVll3WN7zhDbj++utxwQUXYPv27Ugmk7AsC6eeeuqi53KtrOa9t1b23ntv7Nixo2u314v3IRER0UbEEImIiGgdvfSlL8W5556LH/7wh/j85z/f8nLbtm3Dd77zHczPz9dVIz3wwAML/+9Uq1mtDjjgADiOg/322w9/9Vd/1fHtnnDCCbjuuutw99131w3paubrX/86SqUSvva1r9VVsCw1ZK4d27Ztw4MPPrjo/NU8X36/H0960pPw0EMPLQzvWwujo6NNh361U03ypS99CWeccQY++MEPLpxXLBYXDcHrZEazbdu24ec//zls266rmlnNc9nqfrr9mrV7vwBa3vfExERdFVIrnc4S183n1f0Y9t9//4Xzy+UyHnnkka4GaERERG7siURERLSOYrEYrr32WlxyySU48cQTW17uuOOOQ61Ww0c+8pG68z/84Q/DsqyFGd46oTvGjQHDySefDK/Xi3e9612Lqkccx8HMzMySt/vP//zPiEajeM1rXoPdu3cv+v9vfvMbXHXVVQBM1UrjsKvrr7++48fjdtxxx+H//u//cPfddy+cl8vlcN1112HffffFoYce2vK6Dz30EB577LFF56dSKdx9990YHR1dmMVuLRxwwAF44IEHMDU1tXDez372M9x5553LXtfr9S56za655ppFVUytXvtmjjvuOOzatasu5KxWq7jmmmsQi8Vw9NFHL3sb7VjNa7Yae+21F4444gjceOONdc/HL3/5S3z729/Gcccd19btdPKcAt19Xnfs2IFAIICrr7667vX/5Cc/iXQ6jeOPP77t2yIiIuoEK5GIiIjW2RlnnLHsZU488UQ873nPw9vf/nY8+uijePKTn4xvf/vb+OpXv4oLLrigrol2u572tKcBAN7+9rfj1FNPhd/vx4knnogDDjgA73nPe3DRRRfh0UcfxUte8hLE43E88sgj+J//+R+cc845ePOb39zydg844AB89rOfxd/93d/hkEMOwemnn44nPvGJKJfLuOuuuxamMQeAF77whQgEAjjxxBNx7rnnIpvN4t/+7d8wOTmJxx9/vOPHpN761rfic5/7HI499licf/75GBsbw4033ohHHnkE//3f/72oD43bz372M7zqVa/Csccei2c/+9kYGxvDH//4R9x4443405/+hCuvvLLlkK1u+Md//Ed86EMfwjHHHIOzzjoLe/bswcc//nEcdthhC43LWznhhBPwqU99CslkEoceeijuvvtufOc738H4+Hjd5Y444gh4vV68//3vRzqdRjAYxPOf/3xMTk4uus1zzjkHn/jEJ3DmmWfiRz/6Efbdd1986Utfwp133okrr7yyoybqS1nNa7ZaV1xxBY499lhs374dZ511FgqFAq655hokk0lccsklbd2Gfp7OP/98HHPMMfB6vTj11FNbXr6bz+umTZtw0UUX4V3vehde9KIX4aSTTsKDDz6Ij33sY/jrv/5rnHbaaW3fFhERUUd6MiccERHRkNCpue+9994lL9dsSvD5+XnnjW98o7N161bH7/c7Bx10kHPFFVc4tm3XXQ4tpj/ftm2bc8YZZ9Sd9+53v9v5i7/4C8fj8Syaqv6///u/nWc961lONBp1otGo84QnPMHZuXOn8+CDD7b1WH/96187Z599trPvvvs6gUDAicfjzlFHHeVcc801TrFYXLjc1772NedJT3qSEwqFnH333dd5//vf7/zHf/zHouVp9pws9dh+85vfOC972cuckZERJxQKOX/zN3/j3HTTTcsu9+7du533ve99ztFHH+3stddejs/nc0ZHR53nP//5zpe+9KW6yzZOtb7UcjZ7XR555BEHgHPFFVfUnf/pT3/a2X///Z1AIOAcccQRzi233OKcccYZzrZt2xbdpnvq97m5Oecf/uEfnImJCScWiznHHHOM88ADDzR9fv7t3/7N2X///R2v1+sAcG6//XbHcRzn6KOPdo4++uhFz4nebiAQcA4//HDn+uuvb+uxNFvOVtp9zVq9x5tp97Lf+c53nKOOOsoJh8NOIpFwTjzxROe+++6ru8zFF1/sAHCmpqYWXb9arTpveMMbnE2bNjmWZTnuzepW74l2nld9DO7nr9n7znEc5yMf+YjzhCc8wfH7/c7mzZud173udc7c3Nyyj52IiGilLMfpYddDIiIiIiIiIiLqC+yJREREREREREREy2KIREREREREREREy2KIREREREREREREy2KIREREREREREREy2KIREREREREREREy2KIREREREREREREy/L1egH6gW3b+NOf/oR4PA7Lsnq9OEREREREREREXeE4Dubn57F161Z4PEvXGjFEasOf/vQn7LPPPr1eDCIiIiIiIiKiNfH73/8ee++995KXYYjUhng8DkCe0EQi0eOlISIiIiIiIiLqjkwmg3322Wch+1gKQ6Q26BC2RCLBEImIiIiIiIiIBk477XvYWJuIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIiJbFEImIiIiIiIiIaCUcp9dLsK58vV4AIiIiIiIiIqK+NDsrP5NJwDf4EcvgP0IiIiIiIiIiom6rVIBSSX63rN4uyzrhcDYiIiIiIiIiok7lcvIzHAa83t4uyzphJRIRERERERERkarVgGrVnAAgkaivNrJtoFCQ36PR9V/GHmGIREREREREREQEAJkMkM0uPt9xgJER83c+L+f5/UAgsG6L12sczkZEREREREREVCqZAMnnA0IhU2WUz5v+R45jhrLFYuu/nD3ESiQiIiIiIiIiGm6OA6TT8ns0KrOtueVyQCoFTE4CxaIMefN4JGgaIgyRiIiIiIiIiKh/VKvSn6ibzayzWbldrxeIx+v/l0iY4CidNn2SotGhmZVNcTgbEREREREREW0MjiOBjQ4da1QqAXv2ADMz3bvPSgWYn5ffk0mpMHKzLNMPKZ8HymU5b4gaaitWIhERERERERFRb9VqMmQsn5eZzwBgbKx+uJjjyJAyQKqBSiUgGFz6dm1bbjMUkj5HzegwtlCo9fC0YFBCI+2FFA4vDpuGwPA9YiIiIiIiIiLaGDQY2r1bhpTZthki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WiqWZmflVK2u7v41pKpWZdgcQyQiIqIVsRxnrQ73LO+tb30r7rzzTvzv//5v0/87joOtW7fiTW96E9785jcDANLpNDZv3owbbrgBp556Ku6//34ceuihuPfee3HkkUcCAL71rW/huOOOwx/+8Ads3boV1157Ld7+9rdj165dCAQCC/f9la98BQ888MCyy5nJZJBMJpFOp5FIJLr06ImIiIiGQKUiAY5tS4A0Pi5VSI0KBQmPbHvx/yIRGe620vufnZUgyeOR++esbERERAs6yTx6Won0ta99DUceeSRe/vKXY3JyEk95ylPwb//2bwv/f+SRR7Br1y7s2LFj4bxkMomnP/3puPvuuwEAd999N0ZGRhYCJADYsWMHPB4P7rnnnoXLPOc5z1kIkADgmGOOwYMPPoi5ublFy1UqlZDJZOpORERERNShdgMkQKqDNm0C4nE5JRLyE5CAaSXHPUslYHpaAiSfT26fARIREdGK9TRE+u1vf4trr70WBx10EG655Ra87nWvw/nnn48bb7wRALBr1y4AwObNm+uut3nz5oX/7dq1C5OTk3X/9/l8GBsbq7tMs9tw34fbZZddhmQyuXDaZ599uvBoiYiIiIaI9kCybQluxsZaB0jK6zUhUiwmP71eCZBcrQza4jgyJM5xpJH2xASbaRMREa1ST0Mk27bx1Kc+Fe9973vxlKc8Beeccw7OPvtsfPzjH+/lYuGiiy5COp1eOP3+97/v6fIQERER9ZVSaXEFkmeFm53aL0lnVmtXoSD37/NJgLXS+yciIqIFPV2b7rXXXjj00EPrzjvkkEPw2GOPAQC2bNkCANi9e3fdZXbv3r3wvy1btmDPnj11/69Wq5idna27TLPbcN+HWzAYRCKRqDsRERERURuKRdNEOxhcXYAEmCbYpVLzfkmt5HLyMxJZvgKKiIiI2tLTEOmoo47Cgw8+WHfer3/9a2zbtg0AsN9++2HLli247bbbFv6fyWRwzz33YPv27QCA7du3I5VK4Uc/+tHCZb773e/Ctm08/elPX7jM97//fVQqlYXL3HrrrTj44IPrZoIjIiIiolWYnzcBUijU3hC25fh8Us0ESHVROyoVOVmWqWQiIiKiVetpiPTGN74RP/zhD/He974XDz/8MD772c/iuuuuw86dOwEAlmXhggsuwHve8x587Wtfwy9+8Qucfvrp2Lp1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m7k5CXrcbFvOX2qomzsYsizTj2h8XO67XJZqH73tUEiqgtZjJRuJyONLpUzwls/LsurzY1ny/EQia788RERERDRYBrkfktv4eK+XYF11HCL95Cc/wXHHHYd8Po9cLoexsTFMT08jEolgcnKSIRIRdVetJuFQPi9VP4lE/ZCwSkXCGu1pZFkSekQii3sQ6dT2ti23205jab1OqSRBlNcr4dTcnOmnNDq6+HrapNuyzOxlMzNy3syMGTKnolEJbNaT1ysrvXJZlrdQMCt7DdCGoCSXiIiIiNbAsIRIQ6bjEOmNb3wjTjzxRHz84x9HMpnED3/4Q/j9fpx22mn4p3/6p7VYRiIaRtWqVOkUCqY01LYlgAmHJUzK56VnDyBhRzwu/1uuksfj6WxIVjhswiQ1OirLok2z4/H6ZddhbImECWLGxuQ6lYoZHx6JSIDUy3HigYCc9Dn1ell9REREREQrZ9vmIO9KZgSmDavjvZaf/vSn+MQnPgGPxwOv14tSqYT9998fl19+Oc444wycfPLJa7GcRDRMtFpHw6NAQIIWd8VMoWAuHw5LFc969urRSp1UygRZliUrTO3HpLOqKe2jlMlIaBSJbKz+QhrEERERERGthru35kba3qVV6zhE8vv98Pz5TTA5OYnHHnsMhxxyCJLJJH7/+993fQGJaMjUatI3SHsJ6SxlgIRFkYhpCN3rnj2RiFQV5XImSFKWJSFTI4+n+flERERERIOCQ9kGVsch0lOe8hTce++9OOigg3D00Ufjne98J6anp/GpT30KT3ziE9diGYloWDiOVCDZtpS9Nmta7fcDExP1PYp6SfsY6Yxt2jMpFOr9shERERERrTfbNjMiu3uZ0kBou66s9ucZj9773vdir732AgBceumlGB0dxete9zpMTU3huuuuW5ulJKLhMDsrYYzXK/2DluptFAxunJAmmZTAa3RUKqdisd72OCIiIiIi6pVcToIkn29xX1Hqe23v5fzFX/wFzjzzTPzjP/4jjjzySAAynO1b3/rWmi0cEQ2RdFqqiyxLAqSNEhAREREREVF7bFsmxwHk4CoNnLYrkXbu3IkvfelLOOSQQ/DsZz8bN9xwA/JaokZEtBrVqhyxAKSahzM4EBERERH1n/l509s0FOr10tAaaDtEesc73oGHH34Yt912G/bff3+cd9552GuvvXD22Wfjnnvu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5tH2cLbHHnsMxx133MLfO3bsgGVZ+NOf/oS999575UtLREREREREnSmVpBKiUqk/f35e/jc6anZsHcdUKXm9MuTGtoF0WsIiQMIj25bLpdNynmV1FkgRDapyWQIk25bP0Pi4fGaGUNuPulqtItTQKMrv96PS+KVFREREREREayefl+ohQIKeaFRO5bKcXy7LcJtgUEKhZsPcLEvCJQCIxUxYlM8DuZxcJxbr+woLolUrFORz5TgybG1sbKg/F22HSI7j4Mwzz0QwGFw4r1gs4rWvfS2i0ejCeV/+8pe7u4REREREREQkslnT8DoSkX5F2l4kHJYG2HNz9T2NAHMZHbbmOLIjPDpa3zRbA6labah3lGmIOI5U7wWDEq66uT9voZB8XhovM2TaDpHOOOOMReeddtppXV0YIiIiIiIiamF+Xk6AVAk1613i9QITE1I9Ydsy5MbvNyGS48j5+r9WO8QMkGhYpFLyefF45DMVicj56bRU5QESrCaTPVvEjaTtEOn6669fy+UgIiIiIiKiVjIZqYoA2mueHQ43P9+yJCBiSEQkPcW0L5htS6CUzcrno1SS85NJCZEIQAchEhEREREREfWAuyIikZAqJCJaPR2qpkNB5+dNHzHLkuFrDb2hhx1DJCIiIiIioo3Ats2wM5VKSbNrgBURNDh0FsGxscXv+fVSKsnJsiSc9XolTMpmpUIpHq/vF0YAGCIRERERERF1R6kkfYZWMlRMq418Pql8CAYlPNKhNiMjplcLUT+rVk1vr/n53vUacjeo18+s9kWilhgiERERERERrVYuJ0EQIDul8Xj7YVKtZoarVatSCaH9jzikhgaNBkiABKWx2Pr36CoWpdrIspbvL0Z1elQ3RkRERERENCAcx4Q+gOwY79kjoZJtL399DZACARneo5URDJBo0FSrprrO51v82VkvWoUUi/VuOF2fYiUSERERERHRahQKUk3k9cqws2xWhrblcvJzfLx1pYVtmxApFpPASEMjx5EgiWhQaBVSKCTv9+lpef+vdTVStQqUy1J9VCrJ3x4Pm9SvAEMkIiIiIiKi1dBKimhUehkFg7KjmkrJzur0NDAx0XwnOZ+XsEh7IbkxQKJB4q5CiscBv998VubnJYDtNtuWikC9X7dEgp+xFWDdFhERERER0UoVCqaqwT1zWjBogqNaTYKkarX+uo5TX4VE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9NBD8q1vfUu+//3vy7vf/e75egpASzQ6FkREzjrrrJrfFffee2/N5RwLWAoef/xx2bx5s/z4xz+Whx56SMrlsmzcuFFyudz4dRr9bVStVuWcc86RUqkkP/rRj+Suu+6SO++8U2688cZ2PCVgxpo5HkRErrjiiprfD7fccsv4Zcv2ePCx5J1yyin+5s2bx/9frVb9tWvX+jfffHMbtwqYezfddJN/3HHH1b1saGjITyQS/v333z9+3i9/+UtfRPytW7fO0xYC80NE/K997Wvj//c8z1+zZo3/j//4j+PnDQ0N+alUyr/33nt93/f95557zhcR/yc/+cn4dR588EE/Eon4//u//ztv2w60UvhY8H3fv+SSS/y//Mu/nPQ2HAtYqnbv3u2LiP/444/7vt/c30YPPPCAH41G/YGBgfHrfOELX/C7u7v9YrE4v08AaKHw8eD7vv/GN77R/9u//dtJb7NcjwcqkZa4Uqkk27ZtkzPPPHP8vGg0KmeeeaZs3bq1jVsGzI/f/OY3snbtWnn5y18uF110kbz44osiIrJt2zYpl8s1x8bRRx8thx56KMcGlrznn39eBgYGat7/PT09cuqpp46//7du3Sq9vb1y0kknjV/nzDPPlGg0Kk888cS8bzMwlx577DFZtWqVHHXUUXLllVfKvn37xi/jWMBSNTw8LCIi/f39ItLc30Zbt26V9evXy+rVq8evs2nTJhkZGZFnn312HrceaK3w8WDuvvtuWblypRxzzDFyww03SD6fH79suR4P8XZvAObW3r17pVqt1ryxRURWr14tv/rVr9q0VcD8OPXUU+XOO++Uo446Snbu3Ckf//jH5U//9E/lmWeekYGBAUkmk9Lb21tzm9WrV8vAwEB7NhiYJ/Yer/e7wS4bGBiQVatW1Vwej8elv7+fYwRLyllnnSXnn3++HHHEEbJjxw758Ic/LGeffbZs3bpVYrEYxwKWJM/zZMuWLfKGN7xBjjnmGBGRpv42GhgYqPu7wy4DFqN6x4OIyF//9V/LYYcdJmvXrpWnn35arr/+etm+fbv853/+p4gs3+OBEAnAknX22WeP/3zsscfKqaeeKocddph8+ctflnQ63cYtAwAsFBdeeOH4z+vXr5djjz1WXvGKV8hjjz0mZ5xxRhu3DJg7mzdvlmeeeaamVySwXE12PLi979avXy8HH3ywnHHG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yrp16+TXv/61vOpVr5rwGC+88ILEYjFZtWrV+Hm//vWv5cEHH5Qnn3xSTj75ZBER+Zd/+Rd59atfXXPbLVu2jP98+OGHyyc+8Ql573vfK5///OdFROTyyy+X17/+9bJz5045+OCDZffu3fLAAw/I9773PRERefHFF+WVr3yl/Mmf/IlEIhE57LDDJmzf2rVr5YUXXpjJ7gMAAIsclUgAAABNOvbYY8d/jsVismLFClm/fv34eatXrxYRGa8Q+vnPfy6PPvroeI+lbDYrRx99tIiI7Nixo+5jFAoFSaVSNc2/f/nLX0o8HpcTTzxx/Lyjjz5aent7a277ve99T8444wx52cteJl1dXXLxxRfLvn37xiujTjnlFHnta18rd911l4iI/Pu//7scdthhcvrpp4uIVjs99dRTctRRR8n73/9++e///u8J25dOp8fvDwAALC+ESAAAAE1KJBI1/49EIjXnWfDjeZ6IiIyOjsq5554rTz31VM3pN7/5zXhwE7Zy5UrJ5/NSKpWmtW2///3v5c1vfrMce+yx8tWvflW2bdsmt912m4hIzX1dfvnlcuedd4qITmW77LLLxrf7hBNOkOeff17+3//7f1IoFOTtb3+7vPWtb615nMHBQTnooIOmtW0AAGBpIEQCAACYIyeccII8++yzcvjhh8uRRx5Zc8pkMnVv87rXvU5ERJ577rnx844++mipVCqybdu28fO2b98uQ0ND4//ftm2beJ4n//RP/ySnnXaavOpVr5KXXnppwv3/zd/8jbzwwgty6623ynPPPSeXXHJJzeXd3d1ywQUXyBe/+EW577775Ktf/aoMDg6OX/7MM8/I8ccfP5PdAQAAFjlCJAAAgDmyefNmGRwclHe84x3yk5/8RHbs2CHf/e535bLLLpNqtVr3NgcddJCccMIJ8sMf/nD8vKOOOkrOOussec973iNPPPGEbNu2TS6//HJJp9Pj1znyyCOlXC7LZz/7Wfnd734nX/rSl+T222+fcP99fX1y/vnny3XXXScbN26UQw45ZPyyT3/603LvvffKr371K/n1r38t999/v6xZs6Zm2twPfvAD2bhxYwv2DgAAWGwIkQAAAObI2rVr5X/+53+kWq3Kxo0bZf369bJlyxbp7e2VaHTyP8Muv/xyufvuu2vOu+OOO2Tt2rXyxje+Uc4//3x597vfXdN8+7jjjpNPf/rT8g//8A9yzDHHyN133y0333xz3ft/17veJaVSSd75znfWnN/V1SW33HKLnHTSSXLyySfL73//e3nggQfGt3Xr1q0yPDw8YYobAABYHiK+7/vt3ggAAAAECoWCHHXUUXLffffJhg0bWn7/X/rSl+Saa66Rl156SZLJZNO3u+CCC+S4446TD3/4wy3fJgAAsPDF270BAAAAqJVOp+Xf/u3fZO/evS2933w+Lzt37pRPfepT8p73vGdaAVKpVJL169fLNddc09JtAgAAiweVSAAAAMvExz72Mfn7v/97Of300+Ub3/iGZLPZdm8SAABYRAiRAAAAAAAA0BCNtQEAAAAAANAQIRIAAAAAAAAaIkQCAAAAAABAQ4RIAAAAAAAAaIgQCQAAAAAAAA0RIgEAAAAAAKAhQiQAAAAAAAA0RIgEAAAAAACAhv4/95yKU/xFXWwAAAAASUVORK5CYII="/>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span> 
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[ ]:</div>
<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain" tabindex="0">
<pre>({'name': 'Jekyll Tags Front Matter',
  'scope': ['punctuation.output.jekyll',
   'punctuation.tag.jekyll',
   'frontmatter.jekyll'],
  'settings': {'foreground': '#SOME_COLOR_YOU_LINK'}},)</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span> 
</pre></div>
</div>
</div>
</div>
</div>
</div>
</main>
</body>
</html>
