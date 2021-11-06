
This is a demonstration of what I think is a bug in cargo. In the `a/` directory
there's a `.cargo/config` file with bullshit contents. However, cargo doesn't
read this config file so no error is raised (this is done to demonstrate
that cargo doesn't read this config). 

However, moving the same `.cargo/config` directory to the root:

```
cp -r a/.cargo .
```

does raise an error: the config file is not a toml file. I expected the 
`.cargo/config` in the subdirectory to apply to the building of the `a/` crate.





