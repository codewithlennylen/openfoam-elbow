
# OpenFOAM-elbow

Simulation of an incompressible fluid flowing in an elbow

- **Solver**: icoFoam
	 - **icoFoam** is a transient solver for incompressible, laminar flow of Newtonian fluids.  

### Order of operations
```bash
fluentMeshToFoam elbow.msh
```
- Generate mesh

```bash
nano system/ControlDict
```
- Edit the ControlDict file to adjust parameters such as *endTime*, *timeSteps*, etc

```bash
icoFoam
```
- Runs the icoFoam Solver

```bash
paraview
```
- Visualize the results (post-processing)

## Tri mesh

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6cbdd4e0-48c2-4e4e-8b55-b98c39adc041" />

- The mesh comprises trigonal cells


### Velocity

<img width="1158" height="718" alt="image" src="https://github.com/user-attachments/assets/cd6879fa-8f76-4f84-b96a-cb7e6e7830bf" />


### Pressure

<img width="1158" height="718" alt="image" src="https://github.com/user-attachments/assets/9718ac4e-21fa-4996-be56-3e7a52c71dcc" />

## Quad Mesh

You can view more features compared to tri-mesh

<img width="1159" height="775" alt="image" src="https://github.com/user-attachments/assets/2f1fa28f-fb69-4acf-9be6-082f8616acef" />

<img width="1159" height="775" alt="image" src="https://github.com/user-attachments/assets/a1fc576c-fc57-4aca-8d36-c3abe2d2600f" />

## Refined Quad Mesh

You can refine a mesh in OpenFOAM by using the command below. After the `fluentMeshToFoam` command.
```bash
refineMesh - overwrite
```

<img width="1126" height="434" alt="image" src="https://github.com/user-attachments/assets/7f4d23a2-6974-42b3-a321-fda6cdb4b8fd" />

<img width="1162" height="568" alt="image" src="https://github.com/user-attachments/assets/d97dd7b7-274c-45aa-859a-a8d76f5e91fa" />

### Other Notes

- You can convert the results into **VTK** format by running `foamToVTK` in the case directory
	- **VTK (Visualization Toolkit) format** is an open, portable standard for storing scientific visualization data, including 3D meshes, scalar and vector fields.
