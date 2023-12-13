# HFP - Health Facility Profile {#hfp-design}

## Introduction

The Health Facility Profile (HFP) toolkit focuses on implementing integrated, people-centred health facility profiles, providing a comprehensive overview of main healthcare facility's resources, services, and performance indicators.

The World Health Organization (WHO) recognizes the importance of monitoring trends and evaluating progress in healthcare facility management by collecting relevant data through national health information systems. Routine data collected from health facilities, as facilitated by the Health Facility Profile toolkit, offer insights into service utilisation, availability, quality, and coverage. This information empowers healthcare managers for planning resource allocation, identifying bottlenecks in service delivery and responding to public health emergencies.

Unlike quality assurance assessment data, health facility profiles can be routinely reported from the facility or district without undergoing strict protocols for verification and observation for the purpose of routine monitoring and analysis. 

This system design document for the Health Facility Profile toolkit will outline the key components and features of the toolkit, providing a comprehensive overview of its functionality. While we aim to present a detailed configuration of the toolkit's data elements and workflows, please note that this document does not consider the resources and infrastructure needed to implement such a system, such as servers, power, internet connections, backups, training and user support, which can be found in the [DHIS2 Tracker Implementation Guide](https://docs.dhis2.org/en/implement/tracker-implementation/target-audience.html)

In the following sections of this document, we will delve into the specifics of the Health Facility Profile toolkit, including its data capture methods, analysis capabilities, and its role in strengthening healthcare facility management within health systems.

Reference metadata for this toolkit is available at: [dhis2.org/metadata-downloads](https://dhis2.org/metadata-downloads/).

### Acknowledgements

The HFP toolkit for DHIS2 was designed with support from The Global Fund in collaboration with Gavi, the Vaccine Alliance with technical inputs provided by WHO Division of Data, Analytics and Delivery for Impact (DDI). Reviews with Global Fund M&E staff were conducted to find synergies with RSSH M&E Framework & KPIs, C-19 RM M&E framework and gather other partner input. Country learning and field experiences were generously shared by partners at MOH Uganda, HISP Uganda, MOH Lao PDR and HISP Vietnam.

## System design overview

### Background

The Health Facility Profile initiative is born out of a critical necessity—to seamlessly integrate essential health facility attributes data into the national Health Management Information System (HMIS). In the last years, the healthcare landscape underscores the paramount importance of unifying diverse sources of health information for a comprehensive understanding of health service delivery. The primary focus of this initiative lies in recognizing and addressing the pivotal role that health facility attributes play in shaping healthcare accessibility, quality, and responsiveness. The integration of health facility data into the HMIS serves as a linchpin for enhancing the overall efficiency and effectiveness of the healthcare system.

In today's dynamic healthcare environment, the importance of having a centralized repository for health facility attributes cannot be overstated. The integration into the HMIS is designed to streamline data access and analysis, offering a holistic view of healthcare infrastructure readiness, service availability, and emergency preparedness. This approach facilitates evidence-based decision-making at both routine and critical junctures, providing policymakers, administrators, and healthcare professionals with real-time insights into the strengths and potential challenges of health facilities.

Crucially, the Health Facility Profile initiative recognizes the interconnectedness of various factors influencing healthcare delivery, ranging from the accessibility of services to the availability of trained staff and the readiness of infrastructure. By consolidating this information within the HMIS, the initiative seeks to bridge informational gaps, enhance strategic planning, and ultimately contribute to the overall improvement of healthcare services. The integration of health facility attributes data into the HMIS is not merely a technical endeavor; it is a strategic move toward a more integrated, responsive, and data-driven healthcare ecosystem.

### Use case

The Health Facility Profile toolkit within DHIS2 serves as a pivotal tool for streamlining routine health facility data collection and integration into the national Health Management Information System (HMIS). The toolkit is designed to facilitate seamless integration of health facility attributes data, providing a comprehensive view of service availability, infrastructure readiness, and overall facility preparedness. This integration is crucial for enhancing data accessibility and analysis across various healthcare programs and for health planners at different levels.

In countries where routine reporting has been digitized down to the district and health facility levels using DHIS2, the Health Facility Profile toolkit leverages this foundation. This digitization empowers health facilities to periodically self-report metrics, enabling district and higher-level health authorities to respond effectively to healthcare facility needs and optimize service provisioning. The integration of routine Health Facility Profiles (rHFP) data into the national DHIS2 system marks a significant leap forward, fostering enhanced data accessibility and utilization across diverse health programs.

Key features of the Health Facility Profile toolkit that contribute to this flexibility and integration include a dynamic digital questionnaire format. This format allows for the collection of different components of health facility data at different times, catering to specific data needs and facilitating a modular approach to data collection. The toolkit enables countries to add additional questions for more routine monitoring of facility profiles, emphasizing the adaptability of the system to evolving healthcare requirements. Furthermore, the toolkit provides a robust set of indicators and data visualization examples, empowering health planners with the tools needed for in-depth analysis and informed decision-making.

#### Intended users

- **Program managers & staff (national & sub-national):** data users who are responsible for routine analysis of data, using data to improve operations and programme strategies, and providing data-driven feedback to programme staff, including implementing partners, facilities, and other service delivery points
- **Programme data managers**: users who are responsible for overseeing data collection, management, data quality, analysis and reporting functions
- **System admins/HMIS focal points**: MOH staff and/or core DHIS2 team responsible for maintaining and improving data systems for health programmes, integrating data streams into national platforms, providing technical support for system design, adaptation and end user support; and maintaining the DHIS2 system over time 
- **Health facility managers & district health officers**: data collection and analysis for assessment of equipment/service availability, planning and preparedness for both routine or emergency situations

### Design structure

The DHIS2 Health Facility Profile configuration is structured in two (2) major components:

- **Dashboard & indicators:** Example of dashboard for analysis of routine Health Facility Attributes popualted by Program Indicators
- **Tracker program:** DHIS2 tracker program has been configured for individual-level (health facility) data collection. The tracker program can be used with the DHIS2 web or Androids clients

## Dashbaord & Analytics

### Dashboard

The dashboard included in the toolkit serve as an example of integrated analysis of Health Facility Attributes routinely reported within a HMIS for a targeted district

**IMAGES DASHBOARD**

### Analytics

In the context of a cohesive and integrated routine Health Management Information System (rHMIS) at the national level, the Analytics component plays a pivotal role in unlocking the full potential of health facility attributes data. The integration of health facility profiles into the HMIS provides a rich source of information that, when triangulated with other datasets, offers a holistic understanding of the healthcare landscape.

Implementations may vary based on design, relevance, scale, and content, but certain cross-cutting principles and suggestions are applicable across diverse local implementations. The integration of health facility attributes data within the HMIS sets the stage for comprehensive analytics, enabling data triangulation with various other datasets. This approach fosters a more nuanced analysis of healthcare service delivery by triangulating information on service availability, staff distribution, and material resources.

#### Data triangulation

One of the key advantages of data triangulation lies in its ability to provide a multidimensional perspective on healthcare facility operations. By correlating information on service availability with staff distribution, health planners can identify areas of potential service gaps or areas where workforce optimization is needed. Similarly, triangulating material availability data with service and staff information facilitates a deeper understanding of resource allocation and utilization patterns.

In the perspective of an integrated rHMIS at the national level, data triangulation becomes a powerful tool for evidence-based decision-making. This approach enables health authorities to make informed decisions regarding resource allocation, infrastructure development, and service optimization. By leveraging the interconnectedness of health facility attributes data with other datasets, the analytics component not only enhances the granularity of insights but also contributes to a more responsive and efficient healthcare system.

Ultimately, the integration of health facility attributes data into the HMIS, coupled with robust analytics and data triangulation practices, empowers health planners to move beyond isolated metrics and gain a comprehensive understanding of the healthcare landscape. This section explores the significance of data triangulation in the context of the Health Facility Profile toolkit within DHIS2, emphasizing its role in promoting a data-driven and integrated approach to healthcare decision-making.

It is of great importance to underline that the ***triangulation exercise is not able to provide an inferential conclusion***, but, rather, to trigger questions and further research to deepen the type of results one can observe from the mapping - are the key populations at risk (eg children under 5) able to reach a health facility within the national coverage buffer radius? Are the highest deaths linked to a higher concentration of population, to the lack of health staff, or any other geographical factor? It is possible to use two layers to investigate possible environmental and geographical factors in the equation:

- **Landcover layer:** the layer will provide information on the biophysical cover of the area (water, urban areas, forests, etc). The presence of lakes or any other water basin could be important as a factor for malaria.
- **Temperature layer:** temperature, together with any entomological and vector control data could feed into the triangulation exercise to map the presence of vectors in the area.
- **Elevation layer:** like the temperature layer, elevation plays an important role in the vector distribution as well as in the ability to reach the available health facilities. The layer could potentially highlight that although the facilities are covering certain areas within the buffer, the radius only considers the crow’s flight distance between the area and the health center. The presence of mountainous areas could play a role in the health seeking patterns of the population, impacting in turn the health outcomes values.

##### Health staff density VS population map

- **Population layer** (either total population or disaggregated by sex and age if and when relevant). Ensure that a Google Earth account is available to import the population data into the instance from the Google Earth database.
	OR
- **Building footprints layer:** the layer allows users to see what portion of a surface is covered by all the footprints of buildings belonging to the population under analysis. If available, the layer will highlight easily the most remote buildings vs the facilities
- **Facility layer:** Map the geographic location of the facilities and add a radius to highlight the catchment area of the facility. The system defaults the radius to 5000 m, though the implementation should refer to the national policy of standard measurement radio for population served. This approach is particularly recommended where the DHIS2 version is below 2.39 and where there is no capacity to apply the catchment area and distances as available in the CrossCut application.
- **Thematic layer:** choropleth when proportions are under analysis and bubbles when numbers are. The layer will use the indicators of density of health staff (GPs, nurses, midwives, laboratory technicians, etc).

The buffer highlighting the radius of service of the health facilities will highlight any uncovered population, particularly if of high density. 
The density of health staff could be easily colour coded via a legend as per national policy in order to underline the appropriateness of the number of available staff (e.g. less than 25 nurses per 100,000 population can be set as red, and more than 25 per 100,000 population as green - threshold based on [WHO NLiS](https://www.who.int/data/nutrition/nlis/info/density-of-nurses-and-midwives))

**EXAMPLE MAP**

##### Health outcomes/volume of service VS population map

- **Population layer** (either total population or disaggregated by sex and age if and when relevant). Ensure that a Google Earth account is available to import the population data into the instance from the Google Earth database.
- **Facility layer:** Map the geographic location of the facilities and add a radius to highlight the catchment area of the facility. The system defaults the radius to 5000 m, though the implementation should refer to the national policy of standard measurement radio for population served. This approach is particularly recommended where the DHIS2 version is below 2.39 and where there is no capacity to apply the catchment area and distances as available in the CrossCut application. 
- **Thematic layer:** choropleth when proportions are under analysis and bubbles when numbers are. Depending on the available data present in the local HMIS information such as malaria deaths, volume of OPD visits, etc can be plotted.

Similarly to the previous map, the population layer will provide the areas of highest concentration, while the facility layer will present the location of the health facilities providing the relevant services and the buffer of coverage as per national policy. 
Taking into account the example of malaria deaths, the triangulation will show the inhabited areas, the coverage of the facilities providing malaria services, and the health outcome data will plot the areas by number of deaths. In particular, if the national policy states a specific goal to be achieved on the specific indicator, the threshold could be further mapped using a legend separating the facilities achieving the goal and those that are not.

## Tracker

### Tracker Program Structure

The tracker program structure is as follows:

