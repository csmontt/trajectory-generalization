# trajectory-generalization

The raw input corresponds to GPS data. For each user id a trajectory = {P_1, P_2, P_3, ..., P_n} is created, where P_i  denotes a combination of coordinates and time stamps such that P_i  = {x_i, y_i, t_i}. That is, each GPS point contains latitude x_i, longitude y_i and a timestamp t_i).

The steps for generalizing trajectories can be found in  the paper:

    @article{adrienko2010spatial,
    title={Spatial generalization and aggregation of massive movement data},
    author={Adrienko, Natalia and Adrienko, Gennady},
    journal={IEEE Transactions on visualization and computer graphics},
    volume={17},
    number={2},
    pages={205--219},
    year={2010},
    publisher={IEEE}
    }

These steps are:

1. extract characteristic points from the trajectories

2. group the extracted points by spatial proximity

3. extract the centroids (average points) of the point
groups and use them as generating points for
Voronoi tessellation

4. use the resulting Voronoi cells as places for placebased
division of the trajectories into segments

5. for each ordered pair of places, aggregate the
trajectory segments starting in the first place and
ending in the second place

6. measure the quality of the generalization and
improve it if necessary.


