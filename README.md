# Truck-Drone-Tandem-Disaster-Relief-Instances
A repository with instances used for the submitted paper "On delivery policies for a truck-and-drone tandem in disaster relief".

## Instance generation
We generate 100 graphs $G=(L,E)$ with $|L|=16$ nodes, by placing the nodes randomly in a $1000 \times 1000$ square. Afterward, we randomly assign $|V|=5$ nodes to be delivery addresses and one node to be the depot.  
We create sparse graphs since they most resemble real road networks. We keep the graphs connected to ensure feasibility: There is a road between each delivery address and the depot. 
We start with a complete graph and gradually reduce the number of edges to $|E|=36$ by randomly deleting edges that do not disconnect the graph. 

## Settings analyzed
In the computational experiments we defined 8 settings. In the basic setting (Base), the drone is twice as fast as the truck ($\alpha=2$) and $D:=V\cup\{v_0\}$, i.e., the remaining nodes serve exclusively as surveillance nodes. We set the truck speed to 1.
We examine seven additional settings by changing one factor at a time in Base. In four settings, we vary  the drone speed ($\alpha=1$, $\alpha=3$) and the incidence of the parking lots $(|D|=11, |D|=16)$. 
Three further settings refer to widespread network characteristics in the TSP-D literature: the Euclidean metric ($L_2$) for the truck with drone shortcuts as well as the Manhattan metric ($L_1$) for the truck with and without drone shortcuts.  

## Instance usage
Comments within an instance file start with ```<``` and end with ```>``` and have to be ignored by a parser.

Node 1 is the depot ($v_0$) for the truck and drone.
The set of delivery adresses $V$ is defined in the line after ```<V>```.
In the setting where we vary the number of parking lots $|D|=11$, we use the set of nodes defined after ```<D 2/3>``` for $D$. These nodes are randomly assigned with uniform probability and $V \subseteq D$.
The edges of the graph are provided in the ```<adjacency matrix>```.


You are kindly requested to cite this paper if these instances are relevant to your research. 

Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
