# orm-queries-

Operations to perform:
  Apply all migrations: admin, auth, contenttypes, sessions, vege
Running migrations:
  No migrations to apply.
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.models import *
>>> vege=Receipe.objects.all()
>>> vege
<QuerySet [<Receipe: Receipe object (3)>, <Receipe: Receipe object (4)>, <Receipe: Receipe object (6)>, <Receipe: Receipe object (8)>, <Receipe: Receipe object (9)>, <Receipe: Receipe object (10)>, <Receipe: Receipe object (13)>, <Receipe: Receipe object (14)>]>
>>> vege=Receipe.objects.all()[1]
>>> vege
<Receipe: Receipe object (4)>
>>> vege=Receipe.objects.all()[1].receipe_name
>>> vege
'haka-update'
>>> vege=Receipe.objects.all()[1].reciepe_view_count
>>> vege
1
>>> vege=Receipe.objects.all()[2].reciepe_view_count
>>> veg
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
NameError: name 'veg' is not defined
>>> vege=Receipe.objects.all()[2].reciepe_view_count
>>> vege
1
>>> vege=Receipe.objects.all()[2].reciepe_description
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
AttributeError: 'Receipe' object has no attribute 'reciepe_description'
>>> vege=Receipe.objects.all()[2].receipe_description
>>> vege
'half'
>>> vege=Receipe.objects.all()[2].user
>>> vege
>>> vege
>>> vege=Receipe.objects.all()[2].user.username
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
AttributeError: 'NoneType' object has no attribute 'username'
>>> for veg in vege:
...        veg.reciepe_view_count=random.randint(10,100)
...        veg.save()
... 
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
TypeError: 'NoneType' object is not iterable
>>> for veg in vege:
...     veg.reciepe_view_count=random.randint(10,100)
...     veg.save()
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 63, in runsource
    code = self.compile(source, filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 178, in __call__
    return _maybe_compile(self.compiler, source, filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 106, in _maybe_compile
    raise err1
  File "/usr/lib/python3.8/codeop.py", line 93, in _maybe_compile
    code1 = compiler(source + "\n", filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 143, in __call__
    codeob = compile(source, filename, symbol, self.flags, 1)
  File "<console>", line 3
    veg.save()
             ^
IndentationError: unindent does not match any outer indentation level
>>> for veg in vege:
...        veg.rciepe_view_count=random.randint(10,100)
...        veg.save()
... 
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
TypeError: 'NoneType' object is not iterable
>>> exit()
jayendra@jayendra-VirtualBox:~/django_project1/recepe_project$ python3 manage.py shell
Python 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from vege.models import *
>>> vege=Receipe.objects.all()
>>> vege
<QuerySet [<Receipe: Receipe object (3)>, <Receipe: Receipe object (4)>, <Receipe: Receipe object (6)>, <Receipe: Receipe object (8)>, <Receipe: Receipe object (9)>, <Receipe: Receipe object (10)>, <Receipe: Receipe object (13)>, <Receipe: Receipe object (14)>]>
>>> import random
>>> for veg in vege:
...        veg.reciepe_view_count=random.randint(10,100)
... 
>>> for veg in vege:
...        veg.reciepe_view_count=random.randint(10,100)
...        veg.save()
... 
>>> vege=Receipe.objects.all()
>>> vege[0].reciepe_view_count
44
>>> vege[2].reciepe_view_count
66
>>> vege[5].reciepe_view_count
60
>>> vege[1].reciepe_view_count
60
>>> vege[7].reciepe_view_count
66
>>> vege[8].reciepe_view_count
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 450, in __getitem__
    return qs._result_cache[0]
IndexError: list index out of range
>>> vege[4].reciepe_view_count
33
>>> vege=Receipe.objects.all().order_by('reciepe_view_count')
>>> vege
<QuerySet [<Receipe: Receipe object (8)>, <Receipe: Receipe object (13)>, <Receipe: Receipe object (9)>, <Receipe: Receipe object (3)>, <Receipe: Receipe object (4)>, <Receipe: Receipe object (10)>, <Receipe: Receipe object (6)>, <Receipe: Receipe object (14)>]>
>>> vege=Receipe.objects.all().order_by('reciepe_name')
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 1659, in order_by
    obj.query.add_ordering(*field_names)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 2222, in add_ordering
    self.names_to_path(item.split(LOOKUP_SEP), self.model._meta)
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/sql/query.py", line 1725, in names_to_path
    raise FieldError(
django.core.exceptions.FieldError: Cannot resolve keyword 'reciepe_name' into field. Choices are: id, receipe_description, receipe_image, receipe_name, reciepe_view_count, user, user_id
>>> vege=Receipe.objects.all().order_by('reciepe_view_count')
>>> vege
<QuerySet [<Receipe: Receipe object (8)>, <Receipe: Receipe object (13)>, <Receipe: Receipe object (9)>, <Receipe: Receipe object (3)>, <Receipe: Receipe object (4)>, <Receipe: Receipe object (10)>, <Receipe: Receipe object (6)>, <Receipe: Receipe object (14)>]>
>>> vege=Receipe.objects.all().order_by('-reciepe_view_count')
>>> vege
<QuerySet [<Receipe: Receipe object (6)>, <Receipe: Receipe object (14)>, <Receipe: Receipe object (4)>, <Receipe: Receipe object (10)>, <Receipe: Receipe object (3)>, <Receipe: Receipe object (9)>, <Receipe: Receipe object (13)>, <Receipe: Receipe object (8)>]>
>>> vege[0].reciepe_view_count
66
>>> vege[1].reciepe_view_count
66
>>> vege[2].reciepe_view_count
60
>>> vege[3].reciepe_view_count
60
>>> vege[4].reciepe_view_count
44
>>> vege[5].reciepe_view_count
33
>>> vege=Receipe.objects.all().order('-reciepe_view_count')[0:2]
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
AttributeError: 'QuerySet' object has no attribute 'order'
>>> vege=Receipe.objects.all().orderby('-reciepe_view_count')[0:2]
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
AttributeError: 'QuerySet' object has no attribute 'orderby'
>>> vege=Receipe.objects.all().order_by('-reciepe_view_count')[0:2]
>>> vege
<QuerySet [<Receipe: Receipe object (6)>, <Receipe: Receipe object (14)>]>
>>> vege=Receipe.objects.all().order_by('-reciepe_view_count')[0:3]
>>> veg
<Receipe: Receipe object (14)>
>>> vege=Receipe.objects.all().order_by('-reciepe_view_count')[0:1]
>>> vege
<QuerySet [<Receipe: Receipe object (6)>]>
>>> vege=Receipe.objects.all().order_by('-reciepe_view_count')[0:6]
>>> vege
<QuerySet [<Receipe: Receipe object (6)>, <Receipe: Receipe object (14)>, <Receipe: Receipe object (4)>, <Receipe: Receipe object (10)>, <Receipe: Receipe object (3)>, <Receipe: Receipe object (9)>]>
>>> Receipe.objects.filter(reciepe_view_count=55)
<QuerySet []>
>>> Receipe.objects.filter(reciepe_view_count=10)
<QuerySet []>
>>> Receipe.objects.filter(reciepe_view_count=5)
<QuerySet []>
>>> vege=Receipe.objects.all().order_by('-reciepe_view_count')[0:1]
>>> vege
<QuerySet [<Receipe: Receipe object (6)>]>
>>> Receipe.objects.filter(reciepe_view_count=5)
<QuerySet []>
>>> Receipe.objects.filter(reciepe_view_count__gte=5)
<QuerySet [<Receipe: Receipe object (3)>, <Receipe: Receipe object (4)>, <Receipe: Receipe object (6)>, <Receipe: Receipe object (8)>, <Receipe: Receipe object (9)>, <Receipe: Receipe object (10)>, <Receipe: Receipe object (13)>, <Receipe: Receipe object (14)>]>
>>> Receipe.objects.filter(reciepe_view_count__gte=55)
<QuerySet [<Receipe: Receipe object (4)>, <Receipe: Receipe object (6)>, <Receipe: Receipe object (10)>, <Receipe: Receipe object (14)>]>
>>> Receipe.objects.filter(reciepe_view_count=55)
<QuerySet []>
>>> Receipe.objects.filter(reciepe_view_count__gte=55).[0]
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 63, in runsource
    code = self.compile(source, filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 178, in __call__
    return _maybe_compile(self.compiler, source, filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 106, in _maybe_compile
    raise err1
  File "/usr/lib/python3.8/codeop.py", line 93, in _maybe_compile
    code1 = compiler(source + "\n", filename, symbol)
  File "/usr/lib/python3.8/codeop.py", line 143, in __call__
    codeob = compile(source, filename, symbol, self.flags, 1)
  File "<console>", line 1
    Receipe.objects.filter(reciepe_view_count__gte=55).[0]
                                                       ^
SyntaxError: invalid syntax
>>> Receipe.objects.filter(reciepe_view_count__gte=55)[0]
<Receipe: Receipe object (4)>
>>> Receipe.objects.filter(reciepe_view_count__gte=55)[0].reciepe_view_count
60
>>> Receipe.objects.filter(reciepe_view_count__gte=55)[0].receipe_name
'haka-update'
>>> Receipe.objects.filter(reciepe_view_count__gte=55)[0]
<Receipe: Receipe object (4)>
>>> Receipe.objects.filter(reciepe_view_count__gte=55)[0].reciepe_view_count
60
>>> Receipe.objects.filter(reciepe_view_count__lte=55)
<QuerySet [<Receipe: Receipe object (3)>, <Receipe: Receipe object (8)>, <Receipe: Receipe object (9)>, <Receipe: Receipe object (13)>]>
>>> Receipe.objects.filter(reciepe_view_count__lte=55)
<QuerySet [<Receipe: Receipe object (3)>, <Receipe: Receipe object (8)>, <Receipe: Receipe object (9)>, <Receipe: Receipe object (13)>]>
>>> Receipe.objects.filter(reciepe_view_count__lte=55).reciepe_view_count
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
AttributeError: 'QuerySet' object has no attribute 'reciepe_view_count'
>>> Receipe.objects.filter(reciepe_view_count__lte=55)[0].reciepe_view_count
44
>>> Receipe.objects.filter(reciepe_view_count__lte=55)[1].reciepe_view_count
14
>>> Receipe.objects.filter(reciepe_view_count__lte=55)[2].reciepe_view_count
33
>>> Receipe.objects.filter(reciepe_view_count__lte=55)[6].reciepe_view_count
Traceback (most recent call last):
  File "/usr/lib/python3.8/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<console>", line 1, in <module>
  File "/home/jayendra/.local/lib/python3.8/site-packages/django/db/models/query.py", line 450, in __getitem__
    return qs._result_cache[0]
IndexError: list index out of range
