# Atmospheric_General_Circulation

Note 1 : This code was developed for educationnal purposes, and for French students. So the comments in the notebook are in French but the graphics and legends are in English.

Note 2 : If you have any comment/suggestion, if you find this code useful --> please send me an email : mailto:frederic.ferry@meteo.fr

THIS CODE IS NOT FULLY FUNCTIONNAL, YOU WILL HAVE TO CODE SOME MISSING PARTS (THIS SHOULD NOT BE TOO DIFFICULT).

The gridded data needed to run the notebook are NOT provided

Get the CERES data here : https://asdc.larc.nasa.gov/project/CERES/CERES_EBAF_Edition4.1

Get the monthly data here :
- ftp://ftp.cdc.noaa.gov/Datasets/ncep.reanalysis.derived/pressure/air.mon.mean.nc
- ftp://ftp.cdc.noaa.gov/Datasets/ncep.reanalysis.derived/pressure/uwnd.mon.mean.nc
- ftp://ftp.cdc.noaa.gov/Datasets/ncep.reanalysis.derived/pressure/vwnd.mon.mean.nc
- ftp://ftp.cdc.noaa.gov/Datasets/ncep.reanalysis.derived/pressure/omega.mon.mean.nc
- ftp://ftp.cdc.noaa.gov/Datasets/ncep.reanalysis.derived/pressure/shum.mon.mean.nc

Daily NCEP data are available here :
- ftp://ftp.cdc.noaa.gov/Datasets/ncep.reanalysis.dailyavgs/pressure/hgt.XXXX.nc
- ftp://ftp.cdc.noaa.gov/Datasets/ncep.reanalysis.dailyavgs/pressure/air.XXXX.nc
- ftp://ftp.cdc.noaa.gov/Datasets/ncep.reanalysis.dailyavgs/pressure/uwnd.XXXX.nc
- ftp://ftp.cdc.noaa.gov/Datasets/ncep.reanalysis.dailyavgs/pressure/vwnd.XXXX.nc

Replace XXXX by the desired year. The code needs the 2015-2020 daily data. You will have to concatenate the yearly NCEP data in one file with NCO ncrcat command or CDO mergetime command:
- https://linux.die.net/man/1/ncrcat
- https://code.mpimet.mpg.de/projects/cdo/embedded/index.html#x1-930002.2.6

--> files z.nc, t.nc, u.nc, v.nc

--------------------------------------------------------------------------------------------------------------------------------------------------

Notebook 1 (inspired by Stull : https://geo.libretexts.org/Bookshelves/Meteorology_and_Climate_Science/Book%3A_Practical_Meteorology_(Stull)/11%3A_General_Circulation/11.02%3A_Section_3-):
- Study the zonal mean radiative budget from CERES data.
- Derive an analytic approximation of the radiative budget to highlight the radiative differential heating
- Compute the required heat transport by the global circulation to compensate radiative differential heating.

![TOA_rad_budget_zonal_annual_analytic](https://user-images.githubusercontent.com/76565450/196165672-c83ad076-ba6a-4d8d-8cfe-d072f65c5645.png)
![TOA_net_transport_analytic](https://user-images.githubusercontent.com/76565450/196167592-85b7adb2-03a3-4783-b2f7-99496103b92b.png)


--------------------------------------------------------------------------------------------------------------------------------------------------

Notebook 2 : 
- Study zonal mean climatologies of the atmosphere from NCEP monthly reanalysis data

![theta_u_zmean_climatology](https://user-images.githubusercontent.com/76565450/196964611-b008b0eb-b826-4b67-bfad-30d54765d525.png)

--------------------------------------------------------------------------------------------------------------------------------------------------

Notebook 3 : 
- Study the Hadley cell in vertical velocity and meridional wind fields from NCEP monthly reanalysis data
- Compute and study the Meridional Overturning Circulation

![wv_zmean_climatology](https://user-images.githubusercontent.com/76565450/196170449-a76bd9a9-49c4-4d76-8538-26b0f9c1c12f.png)
![psi_zmean_monclim](https://user-images.githubusercontent.com/76565450/162641912-96dcc725-e629-459b-b416-d241c12bb801.gif)

--------------------------------------------------------------------------------------------------------------------------------------------------

Notebook 4 :
- Illustrate the difference between a zonal anomaly and a transient anomaly
- Demonstrate that a field can be decomposed in 4 components (axisymetric and stationnary, transient anomaly of the zonal mean, non-axisymetric transient anomaly, stationnary anomaly of the zonal mean)

![z2015-01-01](https://user-images.githubusercontent.com/76565450/196910830-f5da86aa-c549-409c-91a3-10c6705d6963.png)
![z_decomp_2015-01-01](https://user-images.githubusercontent.com/76565450/196910873-a84fdbd7-37b5-4749-a6a2-bbfea19baf39.png)

--------------------------------------------------------------------------------------------------------------------------------------------------

Notebook 5 :
- Study the stationnary anomalies from zonal mean of the geopotential field
- Compute the streamfunction from zonal and meridional winds and study the stationnary anomalies from zonal mean of the streamfunction field

![z200_anomaly_global_climatology](https://user-images.githubusercontent.com/76565450/196910933-07f50dee-e194-4ae7-bf15-252945121e77.png)

--------------------------------------------------------------------------------------------------------------------------------------------------

Notebook 6 :
- Study the meridional heat and momemtum fluxes by stationnary and transient eddies

![eddy_heat_flux_seasonal](https://user-images.githubusercontent.com/76565450/196911112-fe611049-dbd3-473c-82f5-85d934a39076.png)
![stat_heat_flux_seasonal](https://user-images.githubusercontent.com/76565450/196911251-04d063fc-6aae-4da8-828a-c9cb85627920.png)
![eddy_momentm_flux_seasonal](https://user-images.githubusercontent.com/76565450/196911158-c3890e7c-9f16-4c43-859b-527301b4d647.png)
![stat_momentm_flux_seasonal](https://user-images.githubusercontent.com/76565450/196911228-4c1fa8f7-10e2-44ef-81c9-d95539f4963d.png)
