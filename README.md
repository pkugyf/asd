# asd
df
## requires
[numpy](https://numpy.org/)

[scipy](https://www.scipy.org/)

[matplotlib](https://matplotlib.org/)

## Usage
* Untar *MST.tar.gz* and enter the folder *MST*.
* Run *MST.ipypy* to get velocity coherent manimum spanning trees. Before running, several parameters should be set:

 ####(1)'my_dL', the maximum distance between two nodes to be connected;

 (2)'my_dV', the maximum velocity difference between two nodes to be connected. If you have no velocity information, please set 'my_dV' to -1;

 (3)'filename', the path of your data table. Each line of the table is a node to connect, containing its two-dimension position and velocity in sequence. An example is *lbv.dat*, recording Galactic longitude, Galactic latitude and velocity of ATLASGAL clumps. If you do not have velocity information, please give a table only containing two-dimension position and set 'my_dV' to -1. An example is *lv.dat*, conntaining only Galactic longitude and Galactic latitude;
 
 (4)'l1,l2', x range to find filaments. For instance, if your data have Galactic longitude range from 0 to 60 deg. But you only want to inspect filaments from 10 to 15 deg, you can set 'l1,l2' to 10, 15.
* The output of the code are lists that consist of connectivity of nodes in each filament and a figure showing that. In *branch_list.dat*, each list represents a filament and integers are ids for nodes (if you give 100 nodes, the ids for them will be from 0 to 99 in order). The inner lists with two ids mean that these two nodes are connected.
* A demo figure that shows the MSTs is generated in the folder *fig*. *demo_lbv.png* is the output of the code with current parameters. *demo_lb.png* is the output when changing 'my_dV' to -1 and filename to 'lb.dat'.

