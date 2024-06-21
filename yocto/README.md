## Running the container
```bash
docker run --rm -it \
    --user yocto \
    -v $(pwd):$(pwd) -w $(pwd) \
    --privileged  \
    yocto
```

## Running qemu inside the container
```bash
runqemu qemux86-64 nographic
```