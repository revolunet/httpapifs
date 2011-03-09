HttpApiFs for PyFileSystem
===

Use any remote web server FileSystem with [pyfilesystem][1]

Author : [julien@revolunet.com][2]

**example**

    from fs.httpapifs import HttpApiFS
        
    remoteConfig = {
        'url':'http://server.com/api.php'
        ,'username':'admin'
        ,'password':'verysecretone9'
    }
    # open a connection
    myremotefs = HttpApiFs(**remoteConfig)
    # list a dir
    myremotefs.listdir('/')
    # read a file
    print myremotefs.open('README.txt','r').read()
    # write to a file
    myremotefs.open('writeTest.txt', 'w').write('hello, world')



**Links**

 * our [FileBrowser with PyFS backend][3] demo
 * the [PyFileSystem google group][4]
 * the [PHP backend][5] fot this API
 * the [Django backend][6] for this API

  [1]: http://code.google.com/p/pyfilesystem/
  [2]: mailto:julien@revolunet.com
  [3]: http://filebrowser.demo.revolunet.com
  [4]: http://groups.google.com/group/pyfilesystem-discussion/topics
  [5]: http://github.com/revolunet/filebrowser-php-backend
  [6]: https://github.com/revolunet/django-extjs-filebrowser


