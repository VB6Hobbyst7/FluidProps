# FluidProps
This workbook contains open-source user-defined Visual Basic for Applications (VBA) functions in module 'FluidProps' to accurately calculate the following thermophysical properties, and is usesful for HVAC engineers, meteorologists and others:
- Psychrometrics of moist air
- Atmospheric properties: Wind, temperature and pressure as a function of altitude
- Gases: Dry air and ideal gases
- Water
- Antifreeze coolants
- Refrigerants
- Flow friction in pipes/ducts

### List of functions
- Water_Dens(Tw_K): [kg/m³] Density of fluid water at 101325 Pa
- Water_Cp(Tw_K): [J/(kg·K)] Heat capacity of fluid water at 101325 Pa
- Water_Conduct(Tw_K): [W/(m·K)] Thermal conductivity of fluid water and solid ice at 101325 Pa
- Water_KineVisc(Tw_K): [m²/s] Kinematic viscosity of liquid water at 101325 Pa
- Water_DynaVisc(Tw_K): [Pa·s] Dynamic viscosity of liquid water at 101325 Pa
- Water_Pr(Tw_K): [-] Prandtl number of liquid water at 101325 Pa
- Water_Enth(Tw_K): [J/kg] Specific enthalpy of fluid water  at 101325 Pa
- Vapour_Pws(Tdry_K, Optional ice As Boolean = False): [Pa] Saturation vapour pressure, i.e. the equilibrium water vapor pressure above a flat surface
- Vapour_Cp(Tdry_K): [J/(kg·K)] Heat capacity of water vapour, valid near 101325 Pa
- Vapour_Dv(Tdry_K, Patm_Pa): [m²/s] Vapour mass diffusivity of water vapour in air. A.k.a. diffustion coefficient. Used to calculate Schmidt number
- EthyleneGlycol_VolFraction(Tfreeze_C): [-] Minimum required volume fraction of Ethylene Glycol for freezing point Tfreeze_C, valid at 101325 Pa
- EthyleneGlycol_Dens(T_C, VolFraction): [kg/m³] Density of aqueous solution of ethylene glycol coolant/antifreeze
- EthyleneGlycol_Cp(T_C, VolFraction): [J/(kg·K)] Specific heat capacity of aqueous solution of ethylene glycol coolant/antifreeze
- EthyleneGlycol_Conduct(T_C, VolFraction): [W/(m·K)] Thermal conductivity of aqueous solution of ethylene glycol coolant/antifreeze
- EthyleneGlycol_DynaVisc(T_C, VolFraction): [Pa·s] Dynamic viscosity of aqueous solution of ethylene glycol coolant/antifreeze
- PropyleneGlycol_VolFraction(Tfreeze_C): [-] Minimum required volume fraction of Propylene Glycol for freezing point Tfreeze_C, valid at 101325 Pa
- PropyleneGlycol_Dens(T_C, VolFraction): [kg/m³] Density of aqueous solution of Propylene glycol coolant/antifreeze
- PropyleneGlycol_Cp(T_C, VolFraction): [J/(kg·K)] Specific heat capacity of aqueous solution of Propylene glycol coolant/antifreeze
- PropyleneGlycol_Conduct(T_C, VolFraction): [W/mK] Thermal conductivity of aqueous solution of Propylene glycol coolant/antifreeze
- PropyleneGlycol_DynaVisc(T_C, VolFraction): [Pa·s] Dynamic viscosity of aqueous solution of Propylene glycol coolant/antifreeze
- Refrigerant_Sbubble(Refrigerant, TK): [kJ/kg] Bubble-point entropy, i.e. left side of Ts-diagram
- Refrigerant_Sdew(Refrigerant, TK): [kJ/kg] Dew-point entropy, i.e. right side of Ts-diagram
- Refrigerant_CpDew(Refrigerant, TK): [kJ/(kg·K)] Refrigerant gas-phase specific heat capacity, at dew-point temperature and pressure
- Refrigerant_Hbubble(Refrigerant, TK): [kJ/kg] Bubble-point enthalpy, i.e. left side of Ph-diagram
- Refrigerant_Hdew(Refrigerant, TK): [kJ/kg] Dew-point enthalpy, i.e. right side of Ph-diagram
- Refrigerant_Tdew(Refrigerant, Pa): [K] Dew-point temperature at pressure Pa
- Refrigerant_Pdew(Refrigerant, TK): [Pa] Stauration pressure given dew-point temperature
- DryAir_KineVisc(Tdry_K): [m²/s] Kinematic viscosity of dry air, valid at 101325 Pa
- DryAir_DynaVisc(Tdry_K): [Pa·s] = Dynamic viscosity of dry air, valid at 101325 Pa
- DryAir_Cp(Tdry_K): [J/(kg·K)] Specific heat capacity of dry air, valid at 101325 Pa
- DryAir_Conduct(Tdry_K): [W/mK] Specific heat capacity of dry air, valid at 101325 Pa
- DryAir_Pr(Tdry_K): [-] Prandtl number of dry air, valid at 101325 Pa
- Air_Cp(Tdry_K, HumidRatio): [J/(k·gK)] Specific heat capacity of moist air
- Air_Enth(Tdry_K, HumidRatio): [J/kg dry air] Air specific enthalpy per kg dry air
- Air_DryBulb(Enthalpy_Jkg, HumidRatio): [K] Dry-bulb air temperature
- Air_DensR(Tdry_K, RH, Patm_Pa): [kg/m³] Air density, given RH
- Air_DensH(Tdry_K, HumidRatio, Patm_Pa): [kg/m³] Air density, given humidity ratio
- Air_TdewP(Tdry_K, Pv_Pa): [K] Dew-point (or frost-point) temperature, given parial pressure of vapour
- Air_TdewH(Tdry_K, HumidRatio, Patm_Pa): [K] Dew-point (or frost-point) temperature, given humidity ratio
- Air_TdewR(Tdry_K, RH): [K] Dew-point (or frost-point) temperature, given RH
- Air_TdewW(Tdry_K, Twet_K, Patm_Pa): [K] Dew-point (or frost-point) temperature, given wet-bulb temperature
- Air_HumidRatioR(Tdry_K, RH, Patm_Pa): [kg water vapour / kg dry air] Humidity ratio of moist air, given RH
- Air_HumidRatioD(Tdew_K, Patm_Pa): [kg water vapour / kg dry air] Humidity ratio of moist air, given dew-point temperature
- Air_HumidRatioW(Tdry_K, Twet_K, Patm_Pa): [kg water vapour / kg dry air] Humidity ratio of moist air, given wet-bulb tempeature
- Air_HumidRatioX(SpecificHumid): [kg water vapour / kg dry air] Humidity ratio of moist air, given specific humidity
- Air_RHd(Tdry_K, Tdew_K, Optional ice As Boolean = False): [-] Relative humidity (over liquid water), given dew-point temperature
- Air_RHh(Tdry_K, HumidRatio, Patm_Pa): [-] Relative humidity (over liquid water), given humidity ratio
- Air_RHw(Tdry_K, Twet_K, Patm_Pa): [-] Relative humidity (over liquid water), given wet-bulb temperature
- Air_TwetH(Tdry_K, HumidRatio, Patm_Pa): [K] Wet-bulb temperature, given humidity ratio. Fast iterative reverse calculation by secant method
- Air_TwetR(Tdry_K, RH, Patm_Pa): [K] Wet-bulb temperature, given RH
- Air_TwetD(Tdry_K, Tdew_K, Patm_Pa): [K] Wet-bulb temperature, given dew-point temperature
- Atmos_Pa(Height_over_sea_level_m): [Pa] Estimate of standard-atmosphere barometric pressure as a function of height over sea level
- Atmos_Pa2(Atmos_Pa1, Atmos_T1, Altitude1_m, Altitude2_m): [Pa] Estimate of atmospheric pressure at altitude 1 (e.g. sea level, og building site) given pressure andtemperature at Altitude2 (e.g. station altitude)
- Atmos_T(Height_over_sea_level_m): [K] Estimate temperature as a function of height over sea level. Valid in troposphere (<11km)
- Atmos_T2(Atmos_T1, Altitude1_m, Altitude2_m): [K] Estimate of dry-bulb temperature at Altitude2_m given Tdry1_K at aAltitude1_m. Assumes Environmental Lapse Rate (ELR)
- Wind_Loc2_ms(Wind_Loc1_ms, Alpha_Loc1, Alpha_Loc2, Height_Loc2_m): [m/s] Wind speed at Location 2 given wind speed from 10 m high weather station at Location1.
- OrificeMassFlow_m3s(Tappings_str, DuctDia_m, OrificeDia_m, Tdry_K, RH, Patm_Pa, dP_Pa): [m³/s]  Volumetric air flow rate measured by means of pressure drop over an ISO 5167-1 orifice plate
- Air_DuctFriction(FlowRate_m3s, Diam_m, Roughness_m, Tdry_K, RH, Patm_Pa): [Pa/m] Pressure drop per meter duct, for airflow in ducts
- Water_PipeFriction(FlowRate_m3s, Diam_m, Roughness_m, T_K) [Pa/m] = Pressure drop per meter pipe, for water flow in pipes
- FrictionFactor(Re, relRough): [-] Darcy friction factor for laminar or turbulent flow calculated with the Colebrook-White equation.

### References
References are given for each individual function. Sources include "ASHRAE Fundamentals" handbook, and NIST chem. database

### License & warranty
Free share-alike license (CC BY-SA 4.0): https://creativecommons.org/licenses/by-sa/4.0/. Provided with no warranty of any kind.

### Author
Source code and workbook are copyright peter.schild@oslomet.no
