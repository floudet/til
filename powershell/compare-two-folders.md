# Compare Two Folders

This method allows to recursively compare the contents of two folders:

```posh
PS D:\> $fsoLocal = Get-ChildItem -Recurse -path "D:\FileTransfer\Data\Tests" -name
PS D:\> $fsoRemote = Get-ChildItem -Recurse -path "\\172.16.0.20\Data\Tests" -name
PS D:\> Compare-Object -ReferenceObject $fsoLocal -DifferenceObject $fsoRemote
```

Sample output:

```posh
InputObject                                                 SideIndicator
-----------                                                 -------------
Folder3                                                     <=
Folder2\00_a.xml                                            <=
Folder2\01_b.xml                                            <=
Folder2\01_c.xml                                            <=
Folder3\01_a.xml                                            <=
```

The SideIndicator arrow points to the "side" containing the unique file. In the example above we only have "new" files in the "Reference" folder.

[Source](https://blogs.technet.microsoft.com/heyscriptingguy/2011/10/08/easily-compare-two-folders-by-using-powershell)
