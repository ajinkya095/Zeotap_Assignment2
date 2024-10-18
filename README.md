Application2:Real-TimeDataProcessingSystemfor Weather Monitoring with Rollups and Aggregates
Objective:

Develop a real-time data processing system to monitor weather conditions and provide summarizedinsightsusingrollupsandaggregates.Thesystemwillutilizedatafromthe OpenWeatherMap API (https://openweathermap.org/).
DataSource:

ThesystemwillcontinuouslyretrieveweatherdatafromtheOpenWeatherMapAPI.Youwill need to sign up for a free API key to access the data. The API provides various weather parameters, and for this assignment, we will focus on:
 
●	main:Mainweathercondition(e.g.,Rain,Snow,Clear)
●	temp:CurrenttemperatureinCentigrade
●	feels_like:PerceivedtemperatureinCentigrade
●	dt:Timeofthedataupdate(Unixtimestamp)

ProcessingandAnalysis:

●	ThesystemshouldcontinuouslycalltheOpenWeatherMapAPIataconfigurableinterval (e.g., every 5 minutes) to retrieve real-time weather data for the metros in India. (Delhi, Mumbai, Chennai, Bangalore, Kolkata, Hyderabad)
●	Foreachreceivedweatherupdate:
○	ConverttemperaturevaluesfromKelvintoCelsius(tip:youcanalsouseuser preference).
RollupsandAggregates:

1.	DailyWeatherSummary:
○	Rolluptheweatherdataforeachday.
○	Calculatedailyaggregatesfor:
■	Averagetemperature
■	Maximumtemperature
■	Minimumtemperature
■	Dominantweathercondition(givereasononthis)
○	Storethedailysummariesinadatabaseorpersistentstorageforfurtheranalysis.
2.	AlertingThresholds:
○	Define user-configurable thresholds for temperature or specific weather conditions(e.g.,alertiftemperatureexceeds35degreesCelsiusfortwo consecutive updates).
○	Continuouslytrackthelatestweatherdataandcompareitwiththethresholds.
○	If a threshold is breached, trigger an alert for the current weather conditions. Alertscouldbedisplayedontheconsoleorsentthroughanemailnotification system (implementation details left open-ended).
3.	Implementvisualizations:
○	Todisplaydailyweathersummaries,historicaltrends,andtriggeredalerts.

TestCases:

1.	SystemSetup:
○	VerifysystemstartssuccessfullyandconnectstotheOpenWeatherMapAPI using a valid API key.
2.	DataRetrieval:
○	SimulateAPIcallsatconfigurableintervals.
○	Ensurethesystemretrievesweatherdataforthespecifiedlocationandparses the response correctly.
3.	TemperatureConversion:
 
○	TestconversionoftemperaturevaluesfromKelvintoCelsius(orFahrenheit) based on user preference.
4.	DailyWeatherSummary:
○	Simulateasequenceofweatherupdatesforseveraldays.
○	Verifythatdailysummariesarecalculatedcorrectly,includingaverage,maximum, minimum temperatures,and dominant weather condition.
5.	AlertingThresholds:
○	Defineandconfigureuserthresholdsfortemperatureorweatherconditions.
○	Simulateweatherdataexceedingorbreachingthethresholds.
○	Verifythatalertsaretriggeredonlywhenathresholdisviolated.

Bonus:

●	ExtendthesystemtosupportadditionalweatherparametersfromtheOpenWeatherMap API (e.g., humidity, wind speed) and incorporate them into rollups/aggregates.
●	Explorefunctionalitieslikeweatherforecastsretrievalandgeneratingsummariesbased on predicted conditions.
Evaluation:

Theassignmentwillbeevaluatedbasedonthefollowingcriteria:

●	Functionalityandcorrectnessofthereal-timedataprocessingsystem.
●	Accuracyofdataparsing,temperatureconversion,androllup/aggregatecalculations.
●	Efficiencyofdataretrievalandprocessingwithinacceptableintervals.
●	Completenessoftestcasescoveringvariousweatherscenariosanduserconfigurations.
●	Clarityandmaintainabilityofthecodebase.
●	(Bonus)Implementationofadditionalfeatures.



ArtifactsTobeSubmittedFortheAssignments

●	Codebase-preferablyagithubhandle
●	Readmeshouldbecomprehensive-buildinstructionsanddesignchoicesare mandatory
●	Readmeshouldcontaindependenciestodownloadforsettingupandrunningthe application. E.g a webserver, Database all can be docker or podman containers
