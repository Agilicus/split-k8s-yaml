## split-k8s-yaml

![](logo.png)

We've all been there. We have two enormous YAML
files, each with many documents in them. They have
come from maybe `helm template` or `kustomize`.
We want to see the difference.

If one was running, we could use `kubectl diff`. But,
not here.

So, we can run this tool.

Usage:

```
split-yaml old.yaml new.yaml
diff old new
```

(I use [kdiff3](https://github.com/KDE/kdiff3), you might enjoy [meld](https://wiki.gnome.org/Apps/Meld) if you want a graphical view).

What it does is, for each yaml file on the input, create a directory by the basename of the file, and then split all the objects in it, keeping the names unique (apiVersion/kind/namespace/name).

Enjoy under either the Apache-2.0 license *or* the MIT license, your choice.
