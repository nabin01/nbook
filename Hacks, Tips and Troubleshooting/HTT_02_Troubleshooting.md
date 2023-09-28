# Troubleshooting

Find quick troubleshooting tips and useful commands here!

## JAVA apps rendering issue in Wayland 
For JAVA apps having trouble rendering display on dwm or Sway, set the following environment variable:

```
# Put this in .xinitrc, .xsessionrc, .bash_profile
# or in a similar file
$ export _JAVA_AWT_WM_NONREPARENTING=1

# If the above doesn't work, try setting wmname to LG3D.
# This requires wmname to be installed.
$ wmname LG3D
```

## Node JS

### Fix "error:0308010C:digital envelope routines::unsupported"

```
# Do this in the terminal where you use node commands
# Or set this in your package.json
$ export NODE_OPTIONS=--openssl-legacy-provider
```

### Fix the upstream dependency conflict while installing NPM packages
```
$ npm install --legacy-peer-deps
```

