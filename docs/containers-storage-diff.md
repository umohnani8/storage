## oci-storage-diff 1 "August 2016"

## NAME
oci-storage diff - Generate a layer diff

## SYNOPSIS
**oci-storage** **diff** [*options* [...]] *layerNameOrID*

## DESCRIPTION
Generates a layer diff representing the changes made in the specified layer.
If the layer was populated using a layer diff, the result aims to be
bit-for-bit identical with the one that was applied, including the type of
compression which was applied.

## OPTIONS
**-f | --file** *file*

Write the diff to the specified file instead of stdout.

**-c | --gzip**

Force the diff to be compressed using gzip compression.  If the layer was
populated by a layer diff, and that layer diff was compressed, this will be
done automatically.

**-u | --uncompressed**

Force the diff to be uncompressed.  If the layer was populated by a layer diff,
and that layer diff was compressed, it will be decompressed for output.

## EXAMPLE
**oci-storage diff my-base-layer**

## SEE ALSO
oci-storage-applydiff(1)
oci-storage-changes(1)
oci-storage-diffsize(1)
