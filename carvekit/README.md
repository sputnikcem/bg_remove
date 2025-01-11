# 1 - docker containeri yarat

sudo docker build -t carvekit-docker .

# 2 - docker containerini kullani komutta -v nin sol tarafindaki $PWD/input ve $PWD/outputu istedigin folder ile degistir

sudo docker run  -v  $PWD/input:/input -v $PWD/output:/output carvekit-docker /usr/local/bin/python3 -m carvekit --recursive 1 -i /input -o /output
