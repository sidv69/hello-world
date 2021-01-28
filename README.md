# hello-world
hello-world tutorial
new line
new line
and another new line
```
import bz2
def gen_data(chunks=10, chunksize=1000):
    """Yield incremental blocks of chunksize bytes."""
    for _ in range(chunks):
        yield b"z" * chunksize

comp = bz2.BZ2Compressor()
out = b""
for chunk in gen_data():
    # Provide data to the compressor object
    out = out + comp.compress(chunk)

# Finish the compression process.  Call this once you have
# finished providing data to the compressor.
out = out + comp.flush()
```
