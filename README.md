# hash-file
## Gets file the hash value
# Usage
  npm install hash-file-new

# docs
  methods:
      support enumeration,
      algorithmType:{SHA256,SHA1,MD5}
      
      1. hashFile(synchronous way)
          params:{filepath,algorithm}
          example:
            let fs = require('fs');
            let path = require('path');
            let hashFile = require('hash-file-new');
            // my test file 
            let filePath = path.resolve(__dirname,"./test.txt");
            hashFile.hashFile(filePath,hashFile.algorithmType.SHA256).then(resultHash=>{
                console.log(resultHash)
                // result out:
                70ba0de42b3bc52b74dcb10daa99192a559c7171c3c51526c460c950ea94a8cb
            }).catch(err=>{
                // when occured err
                console.err(err)
            })
            
      2. hashFileAsync(async way)
          params:{filepath,algorithm}
          example:
            let fs = require('fs');
            let path = require('path');
            let hashFile = require('hash-file-new');
            // my test file 
            let filePath = path.resolve(__dirname,"./test.txt");
            let resultHash = hashFile.hashFileAsync(filePath,hashFile.algorithmType.SHA256)
            console.log(resultHash)
            // result out:
            70ba0de42b3bc52b74dcb10daa99192a559c7171c3c51526c460c950ea94a8cb
