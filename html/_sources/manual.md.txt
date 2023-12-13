# User Manual

## Requeriments

**Minimum Requeriments:** Java JRE 11+.

## First look and Set Up

When the PIACERE IDE opens, you can see this window.

![vprin](img/Ventana_principal.png)

In this window, we can see the PIACERE menu embedded in the eclipse toolbar. Furthermore, this IDE have a custom view for PIACERE modelling. We can open this perspective by click in the table icon located in the top right part of the window:

![piacopenpersc1](img/apertura_perspectiva.png)

![piacopenpersc2](img/Perspectiva_Piacere.png)

The next step to setting-up the environment, is to configure the tool’s endpoint. To do this we need to make click on the window menu located in the toolbar and then click on Preferences option.

![appref](img/apertura_preferencias.png)

In the PIACERE menu we can find some options to configure the different tools.

![pref](img/preferencias.png)

You can choose some tool by clicking on the desired tool.

![conpref](img/contenido_preferencias.png)

We can configure host, port, and protocol for each tool. However, for security inspector, we can configure more parameters than in the rest (Enabled, Configured and Entity Type).
When you finish all configurations, you are ready to make the first PIACERE project.
If you open the PIACERE view, you can create a PIACERE project by clicking in the new project’s button. Moreover, we add some shortcuts to create some usual files like DOML file.

![newpro](img/Proyecto_nuevo.png)

When creating a new project, two new files appear: firstly, the .doml file where the code will be added; and secondly, a deploymentConfig.json file, which will be used to enter the keys of the different providers.

![newpro_files](img/jsonconfig.png)

![depconfig](img/deploymentConfig.png)

## IDE usage

### Model files

You can convert doml files to domlx and domlx to doml using the pop-up menu. If you click with secondary button in doml file, you can see the “Generate DOMLX Model” in PIACERE submenu and if you do the same in domlx file you can see the “Generate DOML Model” in PIACERE submenu.
The sequence to make doml or domlx conversion is:

![subdoml](img/Submenu_doml.png)

Name this new file and select “OK”.

![gendomlx](img/Generador_domlx.png)

The following message box will appear.

![domlxsuc](img/generated_doml_success.png)

A new file will appear in the Project Explorer.

![newfdoml](img/doml_newfile.png)

DOML only can be open as text, but DOMLX can be open as tree.

![domlxfile](img/domlx_file.png)

![domlfile](img/doml_file.png)

For open the domlx as tree, you need to click on the file with the secondary button and select open with. Now select infrastructure model editor option.

![tree](img/tree_view.png)

Now you can see the model as tree.

![treedomlx](img/tree_view_doml.png)

### Optimization (KR9)

Secondary button in the .doml file and select “PIACERE” and “Optimize DOML”.

![subdoml2](img/Submenu_doml.png)

Then, a new message appears.

![treedomlx](img/optimized.png)

It is possible save the optimization result on the workspace:

![gopt](img/Guardar_resultado_optimizador.png)

![nopt](img/Nombre_resultado_optimizador.png)

### Validation (KR5)

Also, you can validate the DOML It is possible to generate a .dml file if you have a .dmlx file. Click secondary button and select “PIACERE”, “Generate DOML Model”.

You can choose between Validate model or Validate CSP

![subdomlx](img/validador1.png)

When you save the model validation, a new file is generated in the project that contains the result of the validation.

![valm](img/validador2.png)

![valcsp](img/validador3.png)

### Code Generator (KR3)

This is used by the same submenu as validation.

![subdomlx2](img/Submenu_domlx.png)

When the IaC Code Generator finish, appears a new file with tar.gz extension. In this file we can see the terraform and the ansible configuration.

![ngen](img/nombre_generadorIAC.png)

![gval](img/tar_file.png)

### Security scan (KR6 & KR7)
To this kind of files, you can run a “Perform Security Scan”. To make this action, first of all you need to generate the iac file using the project submenu.

![subiac](img/Security_scan1.png)

![iacname](img/Security_scan2.png)

After this, you can yuse the iac file to perform the security scan using the iac file submenu.

![subiacf](img/Security_scan3.png)

![checks](img/Security_scan4.png)

Finally, you got the result as a pop up message.

![checks](img/scan_success.png)

### Canary Sandbox Environment (KR8)

For using canary sandbox or catalogue, first we need to open the correct view. To do this, we can use the window toolbar menu and click on show view option.

![can1](img/canary/canary1.png)

![can2](img/canary/canary2.png)

In this window you can see all deployments that are currently available. You can add more deployments, or download the current deploy.

![can3](img/canary/canary3.png)

You could “Load Info” of any deployment.

![can4](img/canary/canary4.png)

![can5](img/canary/canary5.png)

Download this information at project desktop.

![can6](img/canary/canary6.png)

![can7](img/canary/canary7.png)

![can8](img/canary/canary8.png)

![can9](img/canary/canary9.png)

Visualize the file info is easy with “Text Editor”.

![can10](img/canary/canary10.png)

A .json file that describes a canary, like this example.

![can11](img/canary/canary11.png)

Using this json configuration we can add the deployment to the canary sandbox environment.

![can12](img/canary/canary12.png)

### Infrastructure Elements Catalogue

When you open the infrasctructure elemeents catalogue, you can see a tab with all items of the Catalogue.

![cat1](img/catalogue/catalogue1.png)

For each of these elements you can show all their properties only with a click.

![cat2](img/catalogue/catalogue2.png)

### Runtime Controller (KR11 & KR12)

In this view you can create a new deployment using the option “Create Deployment”.

![run1](img/runtime/runtime1.png)

You only need a valid URL of a repository

![run2](img/runtime/runtime2.png)

![run3](img/runtime/runtime3.png)

![run4](img/runtime/runtime4.png)

Once it is created you can get more information with secondary button “Get Deployment Details”.

![run5](img/runtime/runtime5.png)

![run6](img/runtime/runtime6.png)

Another option of this view is for launch the Grafana module to control the performance of the deployment.

![run7](img/runtime/runtime7.png)

You need to fill the username and password to use it.

![run9](img/runtime/runtime8.png)

![run9](img/runtime/runtime9.png)

![run10](img/runtime/runtime10.png)

### Graphic representation

A graphical editor has been implemented that allows the visualization of a subset of the entities that make up the infrastructure layer of the DOMLX. To use this tool right click on a doml file -> New -> Representations File:

![GR1](img/greditor/PIACERE_GR0.png)

This new window appears:

![GR2](img/greditor/PIACERE_GR1.png)

Then select your DOMLX file source.

![GR3](img/greditor/PIACERE_GR2.png)

And enter/select the parent folder.

![GR4](img/greditor/PIACERE_GR3.png)

An .aird file will appear in the workspace; double-click on it and the following window will appear

![GR5](img/greditor/PIACERE_GR4.png)

In this window we have to add the DOML file to the project dependencies and a new file will appear in the representations column.

![GR6](img/greditor/PIACERE_GR5.png)

Then, we need to enable it selecting the abstactInfra Layer.

![GR7](img/greditor/PIACERE_GR6.png)

And typing a name for the new graphical representation.

![GR8](img/greditor/PIACERE_GR7.png)

Finally, we obtain the following view of the infrastructure layer.

![GR9](img/greditor/PIACERE8.png)

