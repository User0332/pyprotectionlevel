# PyProtectionLevel

## Install

Install PyProtectionLevel using `pip` with `pip install protectionlevel`. The package module is named `protectionlevel`, so you can import all decorators with `from protectionlevel import *`.

## Docs & Usage

Access modifier support for Python. Includes the following access modifiers as decorators:

- `@protectiondefault` - uses the default protection for the item (private); if used on a class, then all attributes will be private (unless specified otherwise by an attribute decorator)
- `@public` - exposes the attribute of the class even if the class is decorated with `@protectiondefault`
- `@private` - makes attribute private (only the class can access the attribute)
- `@protected` - only the class and subclasses can access the attribute
- `@readonly` - the attribute cannot be set
- `@exposeset(access_modifier)` - Can pass either `protectionlevel.private` or `protectionlevel.protected` as the argument to this decorator. Allows code that falls under the protection level passed as `access_modifier` to get and set the attribute, all other code can only get the attribute.