# wpf-tabcontrol-contextmenu

This sample demonstrates how to configure **context menus** for tab items in **Syncfusion TabControlExt** in a WPF application. The `TabControlExt` control provides built-in context menu support and allows customization of menu items for individual tabs.

## Features in This Sample
- **Built-in Context Menu**: Enable or disable default context menu options for tab items and tab list.
- **Custom Context Menu Items**: Add custom menu items and sub-items to tab headers.
- **MVVM Support**: Bind context menu visibility and customization options to properties in the `ViewModel`.
- **Nested Menu Items**: Create hierarchical context menus with multiple levels.

## Key Properties Used
- **ShowTabItemContextMenu**: Shows or hides the context menu for tab items.
- **ShowTabListContextMenu**: Shows or hides the context menu for the tab list.
- **IsCustomTabItemContextMenuEnabled**: Enables custom context menu items for tab items.
- **DefaultContextMenuItemVisibility**: Controls visibility of default context menu items (Visible or Collapsed).

## XAML Overview
```xml
<syncfusion:TabControlExt ShowTabItemContextMenu="{Binding ShowTabItemContextMenu}"
                          ShowTabListContextMenu="{Binding ShowTabListContextMenu}"
                          IsCustomTabItemContextMenuEnabled="{Binding IsCustomTabItemContextMenuEnabled}"
                          DefaultContextMenuItemVisibility="{Binding DefaultContextMenuItemVisibility}">
    <syncfusion:TabItemExt Header="tabItem1">
        <syncfusion:TabItemExt.Content>
            <TextBlock Text="This is the first tab item content" />
        </syncfusion:TabItemExt.Content>
        <syncfusion:TabItemExt.ContextMenuItems>
            <syncfusion:CustomMenuItem Header="Edit">
                <syncfusion:CustomMenuItem Header="SubItem0" />
                <syncfusion:CustomMenuItem Header="SubItem1" />
                <syncfusion:CustomMenuItem Header="SubItem2">
                    <syncfusion:CustomMenuItem Header="Level 2" />
                </syncfusion:CustomMenuItem>
            </syncfusion:CustomMenuItem>
            <syncfusion:CustomMenuItem Header="Copy" />
            <syncfusion:CustomMenuItem Header="Paste" />
        </syncfusion:TabItemExt.ContextMenuItems>
    </syncfusion:TabItemExt>
</syncfusion:TabControlExt>
```

## How It Works
1. The `ViewModel` exposes properties like `ShowTabItemContextMenu`, `ShowTabListContextMenu`, and `IsCustomTabItemContextMenuEnabled`.
2. These properties are bound to the `TabControlExt` to dynamically control context menu behavior.
3. Custom context menu items are defined inside each `TabItemExt` using `CustomMenuItem` elements.

## Documentation
For more details, refer to the official Syncfusion documentation:  
[TabControl ContextMenu](https://help.syncfusion.com/wpf/tabcontrol/contextmenu)
