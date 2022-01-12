# MyfirstProject
import os
folderpath = r"/boot/New Folder"
os.getcwd()
os.chdir(folderpath)
os.listdir()
list_extension=[]
for fl in os.listdir():
  extension=fl.split(".")[-1]
  list_extension.append(extension)
list_extension=set(list_extension)
len(list_extension)
import shutil
os.chdir(folderpath)
path = folderpath + '_' + 'Arrange'
try:
  shutil.rmtree(path)
  os.mkdir(path)
except:
  os.mkdir(path)
for ex in list_extension:
  print(ex,end=",")
  os.mkdir(path+ '/' + ex)
  for fl in os.listdir():
    if ex in fl:
      try:
        shutil.copy(fl,path + "/" +ex)
      except:
        print("skip")
