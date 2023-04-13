# Accessibility: Toolbars need accessible labelling (`@microsoft/fluentui-jsx-a11y/toolbar-missing-aria-v9`)

<!-- end auto-generated rule header -->

The toolbar role needs an accessible name, especially if there are multiple toolbars on a screen.

## Rule Details

This rule aims to prevent a confusing user experience for tool bars.

Examples of **incorrect** code for this rule:

```jsx
<Toolbar>
    <ToolbarToggleButton appearance="subtle" aria-label="Bold" icon={<TextBold24Regular />} name="textOptions" value="bold" />
</Toolbar>
```

Examples of **correct** code for this rule:

```jsx
<Toolbar aria-label="Subtle">
    <ToolbarToggleButton appearance="subtle" aria-label="Bold" icon={<TextBold24Regular />} name="textOptions" value="bold" />
</Toolbar>
```

```jsx
<Label id="my-label">Subtle</Label>
<Toolbar aria-labelledby="my-label">
    <ToolbarToggleButton appearance="subtle" aria-label="Bold" icon={<TextBold24Regular />} name="textOptions" value="bold" />
</Toolbar>
```

