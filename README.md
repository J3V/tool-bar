# Atom Toolbar

This package provides extensible toolbar for Atom.

![Horizontal](http://f.cl.ly/items/453U17471p0C2P2L0t0c/toolbar-horizontal.png)

![Vertical](http://f.cl.ly/items/3y041V2Y1l1x3B0G0g1u/toolbar-vertical.png)

![Big Icons](http://f.cl.ly/items/3M1x1A0J0r3m0q292728/toolbar-big.png)

![Light Theme](http://f.cl.ly/items/351g2D1f1o3f0O1H0N2b/toolbar-light.png)

# Configuration

### Orientation

* Top
* Right
* Bottom
* Left

### Icon size

* Small *(16px)*
* Big *(24px)*

# Plugins

By itself this package just shows empty bar. To add toolbar to your package use this code:

```coffeescript
atom.packages.activatePackage('toolbar')
  .then (pkg) =>
    @toolbar = pkg.mainModule

    @toolbar.appendButton 'octoface', 'application:about', 'About Atom'
    # Adding spacer
    @toolbar.appendSpacer()
    # Using custom icon set
    @toolbar.appendButton 'gear-a', 'application:show-settings', 'Show Settings', 'ion'
    # Function as a callback
    @toolbar.appendButton 'alert', ->
      alert 'foo'
    , 'Show Alert'
```

You can also prepend buttons/spacers using `prependButton()` and `prependSpacer()` methods.

# Supported icon sets

* [Octicons](https://octicons.github.com/) (Atom's flavour)
* [Ionicons](http://ionicons.com/)
