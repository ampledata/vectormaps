Vector Maps Module
==================

This add-on provides a simple and lightweight UI module which can visualize geographical 
information on a vector-based map. The map is rendered using SVG or VML depending on the 
browser support. No browser plugins are required for the module to work correctly. 

Usage
=====

The module expects geoinformation in the form of a *ISO3166-2 country code* or state code 
in the specified field in order to plot the results on the map. It's possible to define 
an optional countField which allows to process already aggregated results.

Example:

<module name="HiddenSearch" layoutPanel="panel_row1_col1" autoRun="true">
	<param name="search">sourcetype=access_combined clientip=* | geoip clientip</param>
	<param name="earliest">-24h@h</param>
	<module name="VectorMap">
		<param name="map">world</param>
		<param name="field">clientip_country_code</param>
		<param name="backgroundColor">#333333</param>
	</module>
</module>

For a list of all possible module parameters see the module reference at your Splunk
installation once the Add-On is installed.

http://localhost:8000/modules#Splunk.Module.VectorMap

Credits
=======

This module has been created by SPP - http://www.spp.at/

The map rendering is done by using a slightly modified version of the excellent jVectorMap 
jQuery plugin: http://jvectormap.owl-hollow.net/
