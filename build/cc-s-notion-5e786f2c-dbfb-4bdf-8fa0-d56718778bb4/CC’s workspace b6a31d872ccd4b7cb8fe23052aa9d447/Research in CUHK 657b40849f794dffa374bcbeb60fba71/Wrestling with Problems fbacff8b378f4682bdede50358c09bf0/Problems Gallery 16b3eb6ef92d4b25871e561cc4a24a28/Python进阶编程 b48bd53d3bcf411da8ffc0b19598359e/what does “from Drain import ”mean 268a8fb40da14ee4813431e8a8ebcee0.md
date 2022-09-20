# what does “from .Drain import * ”mean?

> One leading dot means the current package where the module making the import exists. Two dots means up one package level. Three dots is up two levels, etc. So if you execute from . import mod from a module in the pkg package then you will end up importing pkg.mod. If you execute from ..subpkg2 import mod from within pkg.subpkg1 you will import pkg.subpkg2.mod. The specification for relative imports is contained within PEP 328.
>