# JavaScript Charts and Stock Chart Change Log


## 3.21.11

*    Some rendering issues because of a bug in new Chrome release fixed.
*    Stock chart event stacking issue fixed.


## 3.21.8

*    accessibleDescription added to AmChart class. It is added as <desc> element of a SVG. Most of screen readers will read this description.
*    Bug fix: link to amcharts (free version) was not updating it’s position if chart area was resized.
*    Bug fix: gridAboveGraphs = true was not working properly on Radar chart.
*    Bug fix: negative fill color of a line graph could be slightly visible on a base value line.
*    Bug fix: stock events which went after event with showOnAxis = true were all stacked on this event even if they were not supposed to be 		on the axis.
*    Bug fix: stock chart with value balloons disabled was not showing event description in a tooltip.


## 3.21.7

*    Bug fix: sometimes, if a scrollbar was moved fast to the right/left edge, the chart showed incorrect selection.
*    Bug fix: in some cases on radar chart, if value axis was logarithmic, one extra grid out of chart bounds was shown.
*    Bug fix: OHLC chart lines can display roll-over balloons now.
*    Bug fix: Trendlines were not showing balloon if thickness of a line was 10 or bigger.


## 3.21.6

*    Bug fix: with ChartCursor property updateOnReleaseOnly set to true Chart scrollbar’s selection used to increase after dragging (only 			with parseDates = false).
*    Bug fix: calling validateNow(true) was not zooming out.
*    Bug fix: duration in the value axis balloon could display decimal values for minutes.
*    Bug fix: with Legend’s property useMarkerColorForLabels set to true label did not change color when graph was hidden.


## 3.21.5

*    Bug fix: cursor balloon sometimes was not displayed when cursor was close to the edge.


## 3.21.4

*    Bug fix: in case ignoreAxisWidth was set to true, vertical axis title was not displayed.
*    Bug fix: value axis of serial and gantt charts was not scrolled properly if maxSelectedSeries was set to some number.
*    Bug fix: Gauge arrow was not appearing when clicking on the legend entry after window was resized.


## 3.21.3

*    Bug fix: chart.clear() was not properly clearing the chart from memory in case chart was create with JSON config.
*    Bug fix: in case precision was set on a Value Axis with small negative numbers, axis labels were not displayed.
*    Bug fix: AmGauge legend was not showing x mark when clicked on legend entry.


## 3.21.1

*    Bug fix: some times “show all” button remained visible on full zoom-out if chart used logarithmic value axis.
*    maxZoomFactor default value changed to  1000000 on Gantt chart. This helps to prevent non-accurate zoom on gantt chart.
*    Bug fix: value axis could go slight out of specified min/max when zooming.


## 3.21.0

*    We changed line smoothing algorithm and now smoothed lines look much better.  Old properties bezierX and `bezierY` of AmCharts class 			are deprecated and the same properties were added for AMSerialChart class. So you can set horizontal and vertical tension of 				smoothed line for each chart individually. By default, the values are undefined and chart sets them to bezierX:4 and bezierY:20 for 		regular charts and bezierX:20 and bezierY:4 for rotated charts.
*    rollOverGuide, rollOutGuide and `clickGuide` events were added to AxisBase class.
*    rollOver, rollOut and click events were added to TrendLine class.
*    Mouse wheel listeners are now added to the document only if mouseWheelZoooEnabled or mouseWheelScrollEnabled is set to true.
*    Bug fix: legendPeriodValueText was not working properly if set individually on a StockGraph.
*    Bug fix: useNegatvieColorIfDown: true was producing some JS errors.
*    Bug fix: when zoomed-in to a very top of value axis, it could exceed maximum value.


## 3.20.20

*    “Zoom out” button sometimes remained visible even when fully zoomed out on a chart with logarithmic axis.
*    Bug fix: strictMinMax with date-based value axis was not working.
*    Bug fix: smoothedLine graphs were not rendered properly in the right-end of a graph when fillAlphawas set to > 0.


## 3.20.19

*    Bug fix: when balloon was close to top edge of the container, it did not change it’s orientation and was hidden behind container area.
*    Bug fix: stock chart’s drawing/erasing buttons were not working properly on IE browsers.
*    Bug fix: adding data to stock chart with usePeriod of ChartScrollbarSettings set to bigger period then minPeriod of Category 					AxesSettings could cause not all data to be shown (when working with small amounts of data).
*    Bug fix: adding data to XY chart with scrollbars when at least one of the axis was date-based was causing stack overflow.
*    Bug fix: legend height fixed with legend’s position set to absolute.
*    Zooming Stock chart with mouse wheel improved.


## 3.20.18

*    In case 3D columns were used and there was a big gap in your data some parts of columns might remain visible while scrolling.
*    Value axis minimum could go below 0 while zooming value axis, even if all the data was positive.
*    Graph balloon was not hidden when showNextAvailable was set to true but there were no more data points.
*    Some of the funnel ticks were shown above the slice.
*    External legend with position set to left/right caused chart not to render.
*    Mouse wheel zoom/scroll improved on stock chart.
*    In case oneBalloonOnly of ChartCursor is set to true, it shows top-most graphs balloon if there are data points at the same position.


## 3.20.17

*    forceGap property added to AmGraph. If this is set `true`, the graph will always break the line if the distance in time between two 			adjacent data points is bigger than `gapPeriod x minPeriod`, even if `connect` is set to `true`.
*    Bug fix: bulletColor was not respected if lineColorField was set.
*    Bug fix: logarithmic axes of XY chart were zoomed-in incorrectly after data update.


## 3.20.16

*    Bug fix: class names were not added on Stock chart’s scrollbar even if chart.addClassNames was set to true.
*    Bug fix: toggling parseDates from true to false on CategoryAxis could result JavaScript error.
*    amcharts-scrollbar-horizontal and amcharts-scrollbar-vertical class names added to <g> of Scrollbar (depending on orientation of a 			scrollbar).


## 3.20.15

*    Export plugin updated.


## 3.20.14

*    Gantt chart was ignoring some of the fields like descriptionField, fillColorsField, etc.
*    Min/max values of value axis could change on zoom-out to some different values comparing with initial.
*    In some rare cases legend entries were arranged incorrectly.
*    Plugins updated.


## 3.20.13

*    Fix: In case value axis had minimum/maximum set but real values were of a much bigger scale, chart performance used to drop 					significantly.
*    Pie chart labels now trigger rollover/click events, same as Funnel chart.
*    vResizeCursor with default value ns-resize and hResizeCursor with default value ew-resize added to ChartScrollbar.
*    vResizeCursorHover, hResizeCursorHover, vResizeCursorDown and hResizeCursorDown properties added to ChartScrollbar. You can set CSS 			value and show different mouse pointers on roll-over and on click when using scrollbar grips. Default values are not set.
*    Default value of dragCursorHover changed to cursor: move; cursor: grab; cursor: -moz-grab; cursor: -webkit-grab
*    Default value of dragCursorDown changed to cursor: move; cursor: grab; cursor: -moz-grabbing; cursor: -webkit-grabbing
*    Bug fix: stacked step graphs sometimes drew wrong fills.
*    Bug fix: not all strings were translated if multiple languages on the same page charts were used.
*    centerRotatedLabelsproperty was added to AxisBase. In case you have rotated labels on horizontal axis, you can force-center them using 		this property.
*    Bug fix: it was impossible to click links in balloons.
*    Stock chart performance with equalSpacing set to true improved.
*    You can now access data items from data provider of Stock chart from which aggregated data for longer period was generated: 					dataItem.dataContext.rawData will hold array of raw data items.


## 3.20.12

*    Bug fix: In some cases scrolling Serial chart with labelText set on AmGraph could result JS error.
*    Export plugin updated.


## 3.20.10

*    bandGradientRatio added to GaugeAxis and gradientRatio added to GaugeBand, allows creating radial gradients on bands.
*    setStartValue(value) and setEndValue(value) methods added to GaugeBand. You can use them to create fine animations of your bands.
*    Bug fix: If usePrefixes was set to true for GaugeAxis, it displayed numbers incorrectly.
*    Bug fix: Legend was not firing roll-over and roll-out events if graph or slice was hidden.
*    Bug fix: in some specific cases, when value axis without a graph was added to a chart, zoom-out button was not hidden even if user 			clicked on it.
*    Bug fix: XY chart was not firing inited event if rendered in a hidden container.
*    Bug fix: themes were broken after clear() method of stock chart was called.
*    Bug fix: pie chart with additional legend items added using legend.data property was not hiding/showing slices when clicked on legend 			entry.
*    Bug fix: if a chart was in a scrollable container, mouse wheel scrolling was not working on Chrome.
*    Bug fix: mouseWheelZoomEnabled and mouseWheeScrollEnabled properties of PanelsSettings were not working properly on Stock chart.
*    Bug fix: JS error occurred if maximum of ValueAxis was set to 0 and graph had only positive values.
*    Bug fix: it was impossible to set custom markers for legend entries if useGraphSettings was set to true.
*    Bug fix: Stock chart was treating null values as 0.
*    Bug fix: stacked step graphs with fillColorsField or dashLengthField or some other fields set were drawing fills incorrectly.


## 3.20.9

*    combineLegend property with default value false added. If you set it to true, and you have some legend items set using legend.data 			property, both graph’s entries and those added using data property will be displayed.
*    If showAllValueLabels of AmGraph is set to true, labels which are outside plot area will now also be displayed.
*    Grid synchronization when synchronizeGrid is set to true improved.
*    legendColorFunction added for AmGraph. It is called and the following attributes are passed: dataItem, formattedText, periodValues, 			periodPercentValues. It should return hex color code which will be used for legend marker.
*    Bug fix: funnel chart displayed balloon in a wrong position if labels were disabled.
*    Bug fix: Gauge chart was not displaying axis values if usePrefixes was set to true on GaugeAxis.


## 3.20.8

*    You can use absolute urls for ChartScrollbar dragIcon.
*    Improved grid synchronizing of multiple value axes (when synchronizeGrid of AmSerialChart is set to true).
*    Bug fix: bullets with custom alpha were gaining default opacity on roll-out.
*    Bug fix: stock clear()  method was not clearing it’s own instance from AmCharts.charts array.
*    Bug fix: Axes labels were not firing click events on iOS touch devices.
*    Bug fix: If topMargin was set on PanelsSettings of Stock chart, temporary trend line (while drawing) had wrong y offset.


## 3.20.7

*    columnIndexField added to AmGraph. You can use it with non-stacked column graphs and specify order of columns of each category.
*    Bug fix: logarithmic value axis balloon was not respecting precision setting, same with axis with useScientificNotation set to true.
*    Bug fix: Legend with equalWidths set to false had labels overlapping with values.
*    Bug fix: if newStack property was set on a first graph of value axis, chart produced a gap before the column.
*    Bug fix: lineColorField was not respected by OHLC graph type.


## 3.20.6

*    Bug fix: zoom-out button was sometimes visible with logarithmic scale value axes even if it was fully zoomed-out.
*    Bug fix: when zooming value axes, 3D columns were cropped incorrectly in some cases.
*    Bug fix: maxSelectedSeries setting was not properly working with ChartScrollbar.


## 3.20.5

*    Improved mouse-wheel scroll with parseDates set to true, especially when gaps between data points were bigger than minPeriod duration.
*    Bug fix: if updateOnReleaseOnly of value scrollbar was set to true, chart was not updated if grips were dragged to min/max of value 			axis.
*    Bug fix: with equalWidths of AmLegend set to true, legend items were not properly positioned in case markerWidth was set to some bigger 		value.
*    Bug fix: sum was incorrectly calculated if a graph was hidden and periodValueText was set to “sum”.
*    Bug fix: PeriodSelector’s predefined periods were selecting one day less in some cases.


## 3.20.4

*    A lot of improvements related with charts and maps accessibility:

*    tabIndex property added to: AmLegend, AmGraph, Title, Label, AmSlicedChart, ChartScrollbar and ChartCursor. In case you set it to some number, the chart will set focus on this element when user clicks tab key (after setting focus on all elements with lower tabIndex). When a focus is set, screen readers like h NVDA Screen reader will read label which is set using accessibleLabel property of the same elements. In case it’s ChartScrollbar or ChartCursor, you will be able to move Scrollbar or Cursor with cursor keys of your keyboard.  Note, at the moment not all browsers support tabIndex on SVG elements. At the moment Chrome and Opera do support this well. Here is full compatibility table.
*    zoomOutButtonTabIndex added to AmRectangularChart. In case you set it to some number and user presses tab, the page will set focus on 			the zoom-out button once the browser will reach tabIndex. When focused, pressing enter will result zoom-out of the chart.
*    accessibleLabel property added to AmLegend, with default value [[title]]. This label will be read by screen reader if chart.accessible 		is set to true (default) and user rolls-over the legend marker or focuses on it using tab key (in case tabIndex is set on AmLegend).
*    accessibleLabel property added to ChartScrollbar with default value Zoom chart using cursor arrows.
*    accessibleLabel of AmGraph default changed to [[title]] [[category]] [[value]]
		Other changes:

*    autoTransform property added to AmChart with default value false. If you set it to true and your chart div (or any of the parent div) 			has css scale applied, the chart will position mouse at a correct position. Default value is false because this operation consumes 			some CPU and quite a few people are using css transfroms.
*    synchronizeGrid property with default value false added to AmSerialChart. If your chart has more than one value axes and you set this 			property to true, the chart will show grid at equal intervals. Note, this is experimental property in beta stage yet.
*    Bug fix: if pie chart had depth3D set and marginBottom was set to 0, 3D part of a pie was hidden below the div area.
*    Bug fix: if a slice of a pie was pulled-out initially, hovering over this slice showed moving balloon even if balloon.fixedPosition was 		set to true.
*    Bug fix: panning of a AmRectangularChart (if enabled) was broken since last version.


## 3.20.3

*    Improved behavior of date-based axes when minPeriod is set to milliseconds (“fff”).
*    Improved zoom with mouse wheel, now the chart respects selected range and adjust zoom step according to it – bigger step if long range 		of data selected, smaller step when less data selected.
*    balloonTextFunction added to ValueAxis, you can use it to format any value axis balloon text.
*    Bug fix: since 3.20.1 zooming of non-date-based serial chart with mouse wheel was broken.
*    Bug fix:if useLineColorForBulletBorder of AmGraph was set to true and negativeLineColor was used, bullet borders used positive line 			color instead of negative.
*    Another memory leak problem fixed (happened if you have export enabled and then created a chart and destroyed it by calling 					chart.clear() method).


## 3.20.2

*    Memory leak problem fixed (happened if you created a chart and then destroyed it by calling chart.clear() method).


## 3.20.1

*    Zooming of serial charts with mouse wheel improved – the chart zooms to the position of the mouse instead of simply zooming to the 			center. Note, mouseWheelZoomEnabled property of a chart must be set to true in order this to work.
*    value step of a logarithmic value axis improved.
*    In case useMarkerColorForValues property of AmLegend is set to true, value labels now respect color of data item.
*    In case useMarkerColorForLabels property of AmLegend is set to true, both label and marker will change color to data item color. This 			is useful when you have a different negativeFillColors set on AmGraph and want this to be reflected in a legend.
*    Bug fix: wrapped data labels inside columns were not vertically aligned.
*    Bug fix: Radar chart was not displaying value axis title properly.


## 3.20.0

*    Since v 3.20.0 we added basic support of accessibility.
*    Property accessible added to AmChart class, with default value true. When enabled, chart adds aria-label attributes to columns, bullets 		or map objects. You can control values of these labels using properties listed below. Note, not all screen readers support these 			tags. We tested this mostly with NVDA Screen reader. WAI-ARIA is now official W3 standard, so in future more readers will handle 			this well. We will be improving accessibility on our charts, so we would be glad to hear your feedback.
*    Property, accessibleTitle added to AmChart class. This title will be read by screen reader.
*    Property accessibleLabel added to AmGraph class, with default value [[title]] [[value]].
*    Property accessibleLabel added to AmSlicedChart class, with default value [[title]]: [[percents]]% [[value]] [[description]]
*    Bug fix: in some particular cases angular gauge was changing it’s position incorrectly while changing size of chart container.
*    Bug fix: YTD button of PeriodSelector was not hidden even if no this year’s dates were available in the data.
*    Bug fix: touchDuration property was affecting also clicks, not only touch events.


## 3.19.6

*    default value of svgIcons of PanelsSettings was changed to true.


## 3.19.5

*    animate plugin added to amcharts package, allows creating animated transitions from one data to another.
*    properites minMarginLeft, minMarginRight, minMarginTop and minMarginBottom added to AmRectangularChart chart. If left side has a value 		axis and autoMargins is set to true (default), the margin of this side will be not less than set on minMarginLeft property, same 			with other sides.
*    smoothedLine graph type now supports gradients
*    color property added to GaugeAxis, specifies labels color of the axis.
*    axisFrequency property added to ValueAxis, works with Radar chart only. If you have a big number of axes, this property will help you 			to show every x axis only.
*    Bug fix: enabled property of ChartCursor was not working properly (if set to false).
*    Bug fix: class name amcharts-balloon-div-[id] (where id is graph or axis id) was not set.
*    Bug fix: in some particular cases axis guides might become invisible.
*    Bug fix: a very quick scrollbar movement in some setups could produce JavaScript error.
*    Bug fix: tapToActivate was not working properly on some devices.
*    Bug fix: sometimes if zooming near the edges of the chart container div with ChartScrollbar, some of the data points were left outside 		the plot area.
*    Bug fix: minor grid of logarithmic axis was not drawn properly.


## 3.19.4

*    New property, bulletHitAreaSize added to AmGraph. Default value not set. Useful for touch devices – if you set it to 20 or so, the 			bullets of a graph will have invisible circle around the actual bullet (bullets should still be enabled), which will be easier to 			touch (bullets usually are smaller and hard to hit).
*    Bug fix: radial gradients of pie chart were shifted to incorrect position in some cases.
*    Bug fix: chart.removeLegend() removed legend but did not expand chart area properly.
*    Bug fix: if limitToGraph was set on ChartCursor and the graph was hidden, JavaScript error was produced.
*    Bug fix: in some cases, when equalSpacing of CategoryAxis was set to true, first label of an axis was made bold even if it shouldn’t to 		be bold.


## 3.19.3

*    New property, touchClickDuration added to AmChart class. Default value is 0, but if you set it to 200 (milliseconds) or so, the chart 			will fire clickGraphItem or clickSlice (AmSlicedChart) only if user holds his finger for 0.2 seconds (200 ms) on the colum/bullet/			slice.
*    Touch events behavior improved. clickGraphItem event will not be fired if user moved a finger (dragged or selected) over a chart.
*    Bug fix: radial gradients of pie chart were shifted to incorrect position on Safari.
*    Bug fix: Firefox produced JavaScript error if chart was loaded in a hidden iFrame.


## 3.19.2

*    Code cleanup.


## 3.19.1

*    JS error could occur in some cases if responsive plugin was used.


## 3.19.0

*    dragCursorHover with default value cursor: cursor: grab; cursor:-moz-grab; cursor:-webkit-grab; and dragCursorDown with default value cursor: cursor: grab; cursor:-moz-grabbing; cursor:-webkit-grabbing; properties added to ChartScrollbar. This enables hand cursor when hovering over the selected area of ChartCursor. Does not work with some older browsers.
*    Patterns now supports URI.
*    Bug fix: time stamp instead of Date Object was passed to  categoryBalloonFunction of CategoryAxis.
*    Bug fix: angular gauge changed it size after chart.invalidateSize() method was called, event if the size of the div was not changed.
*    Bug fix: minSelectedTime and maxSelected time was ignored by ChartScrollbar.
*    Bug fix: legend was not properly displayed if legend.position was changed at run time.
*    Bug fix: XY chart was not adjusting margins if on initial render the chart div was not visible.
*    Bug fix: export problem with XY chart fixed.
*    Bug fix: axis labels were drawn differently from initial view after the chart was zoomed-in and then zoomed-out.
*    Bug fix: axis was not always firing axisZoomed event;
*    Bug fix: legend marker switch position was not exactly in the center of the marker in some cases.
*    Bug fix: grid was overlapping data labels in some cases.
*    Bug fix: Some issues with Mekko chart and empty values fixed.
*    Bug fix: Gant chart produced JavaScript error if dataProvider was undefined.
*    Bug fix: With equalSpacing set to true, predefined period of StockChart was not always properly selected.


## 3.18.6

*    Bug fix: it was impossible to turn off category balloon by setting categoryBalloonEnabled property of ChartCursor to false if initially it was set to true.
*    Bug fix: roll-over balloon was not displayed if a fixedPosition of AmBalloon was set to false and the column’s top was out of plot area.
*    Bug fix: if equalSpacing of CategoryAxesSettings was set to true (Stock chart) default period was not always correctly set.
*    Bug fix: AmGanttChart produced JS error if no dataProvider was set.
*    Data loader and export plugins updated.


## 3.18.5

*    Minor bug fix release


## 3.18.4

*    Bug fix: In case data loader plugin was used, chart could generate JavaScript error if user hovered over chart while loading data.
*    Bug fix: zoom-out button was sometimes visible even the chart was fully zoomed-out.
*    Bug fix: glueToTheEnd of Stock chart was not functioning properly when set to true.
*    Bug fix: value axis balloon (if enabled) was visible ant pointed to a wrong position when cursor was shown using cursor.showCursorAt(*  		category) method.
*    Bug fix: onePanelOnly of ChartCursorSettings was not working when set to true.
*    Bug fix: in some particular cases letters of Stock events were disappearing when moving mouse over plot area.
*    Bug fix: categoryBalloonFunction of ChartCursor was not working unless categoryBalloonText was set to undefined.
*    Solved conflict with prototype.js library.


## 3.18.3

*    Stock chart legend did not reset value text to periodValueTextRegular after data sets were compared.
*    Improved filling of a graph if fillColorField is set.
*    Graph balloon is now hidden if user rolls-over StockEvent icon.
*    Bug fix: graphBulletSize of ChartCursor was ignored when valueBalloonsEnabled was set to false.
*    Bug fix: when labelText was set on AmGraph, it used to draw empty text nodes for each data point, even if no text was displayed.
*    Bug fix: “changed” event was not fired by AmSerialChart.


## 3.18.2

*    Bug fix: JS error happened if stacked column chart has column with 0 value and labels on columns were enabled.
*    Bug fix: axis.balloon.enabled = false did not disabled axis balloons.
*    Bug fix: minor grid on logarithmic axis was drawn chaotically in some cases.
*    Bug fix: if logarithmic axis had treatZeroAs set, axis was not zooming.
*    Bug fix: valueLineBalloonEnabled of ChartCursor was not applied if changed from true to false at run time.
*    Bug fix: Stock event balloon was not hidden on roll-out.
*    improved animations when limitToGraph is set on ChartCursor.


## 3.18.1

*    Bug fix: zoom-out button was disappearing after chart.validateData() call on XY chart.


## 3.18.0

*    Changes at a glance:
*    Code cleanup and restructure for better performance, smaller files, reduced memory use!
*    Smoother animation!
*    Pinch-zoom on phones, tablets and desktops (the latter is Chrome only for now)!
*    Zooming/scrolling of ValueAxis on Serial and GANTT charts!
*    Improved zooming of logarithmic value axes.
 

*    All changes:
*    valueScrollbar added to SerialChart. Adds ChartScrollbar to ValueAxis. You can set autoGridCount to true to enable axis labels. This 	trick can also be used by XY chart (albeit by using regular chartScrollbar property, not valueScrollbar). Here is a demo of serial chart with value scrollbar.
*    valueZoomable property added to ChartCursor (default: false). If set to true, makes the cursor zoom value axis(es) as well. Works best if valueScrollbar is added to a chart. Here is a GANTT chart with zoomable value axis.
*    You can now pan XY chart with chart cursor (previously it was only possible to select area for zoom-in). To enable this feature, set pan property of ChartCursor to true. To enable pan of value axis on Serial chart, set valueZoomable of ChartCursor to true. XY Chart with pan enabled demo.
*    maxZoomFactor is now property of AmRectangularChart, with default value 20. Specifies max zoom factor of ValueAxis.
*    drop property (default: false) added to AmBalloon (not supported by IE8). Allows having drop-shaped balloons. Note, these balloons will not check for overlapping with other balloons, or if they go outside plot area. It also does not change pointer orientation automatically based on its vertical position like regular balloons do. You can use pointerOrientation property if you want it to point to different direction. Demo of a chart using this kind of balloon.
*    pointerOrientation property added to AmBalloon, with default value down and other possible values "up", "down", "left", and "right". Works only if balloon.drop set to true.
*    zoomOutValueAxes() method added To AmRectangularChart. When invoked, it zooms-out value axes.
*    gradientType added to AmPieChart. The default is now at “radial”. (previously chart supported only linear gradients) It makes a lot more sense to have radial gradients on pie chart. Note, IE8 does not support this. Here is pie chart with gradient fill example.
*    minValue and maxValue properties added to AmXYChart. These can be used to adjust size/scale of bubbles. If these properties are not set, the bubble with smallest value will be of minBulletSize and bubble with biggest value will be of maxBulletSize. However, you might want bubble size to change relative to 0 or some other value. In this case you can use minValue and maxValue properties. Note, if you use these two settings, you might also want to set minBulletSize to 0.
*    balloonText property added to TrendLine. When set, enables displaying a roll-over balloon.
*    onShowCursor, zoomStarted, panning events added to ChartCursor.
*    limitToGraph property added to ChartCursor. If set to an id or a reference to AmGraph object, CategoryAxis cursor line will be limited to this graph instead of being drawn through full height of plot area. Note, this works with serial chart only. Also, cursorPosition of ChartCursor must be set to middle.
*    syncWithCursor(cursor) method added to ChartCursor. Allows to sync one serial chart’s cursor with another chart’s cursor.
*    balloon property added to AmGraph and AxisBase. Allows customizing axes and graphs balloons individually (only when ChartCursoris used). Note: the balloon object is not created automatically, you should create it before setting properties, for example: graph.balloon = {drop:true} and not graph.balloon.drop = true.
*    valueLineBalloonEnabled now adds value balloons to all available value axes (both Serial and XY chart).
*    animationFinished event added to AmChart. It is dispatched when graphs or slices finish animating.
*    zoomOutAxes property added to PanelsSettings (default: true. Specifies if zoomed-in value axes should be zoomed-out when user changes selected period with PeriodSelector.
*    processTimeout property added to AmChart and AmStockChart (default: 0). If you set it to 1 or some bigger value, chart will be built in chunks instead of all at once. This is useful if you work with a lot of data and the initial build of the chart takes a lot of time, which freezes the whole web application by not allowing other processes to do their job while the chart is busy.
*    Serial chart now has property processCount (default 1000). If processTimeout is > 0, 1000 data items will be parsed at a time, then the chart will make pause and continue parsing data until it finishes.
*    buildStarted event added to AmChartand AmStockChart. Fired just before the chart starts to build itself for the first time. Note: you might need to set processTimeout to > 0 value in order to register this event properly.
*    You can set categoryAxisDateFormat of ChartCursor to undefined now. If set cursor’s category axis balloon will use current date format of category axis.
*    Changed default behavior: the order of the graphs is now determined by the order they are defined in graphs array, regardless of graph type. Previously line graphs always came on top unless specifically specified to go under columns.
*    Bug fix: chart cursor was not working properly on mekko chart (variable column width chart).
*    Bug fix: addressed pan freezing issues introduced in Chrome v47.
*    Bug fix: Microsoft Edge was ignoring touch-move events.
*    Bug fix: stacked areas on date-based chart could start on wrong place after graph was hidden.
*    Bug fix: AmAngularGauge was broken if legend was added.
*    Bug fix: showNextAvailable property of ChartCursor was ignored by legend.
*    Bug fix: Pyramid chart did not display the tip of the pyramid in some cases.
*    Bug fix: init event was not fired by AmAngularGauge.
*    Bug fix: sometimes init, rendered and draw events were fired too early, before the chart was actually drawn.
*    Bug fix: mouse wheel zoom was not working on IE8.
*    Bug fix: if autoSize of AmChart was set to false, mouse position was not properly detected after page was scrolled.
*    Bug fix: selectFromStart property of PeriodSelector was not working properly with period button which used YYYY period.
*    Bug fix: it was impossible to delete guides which were added via chart config (using eraser tool of Stock chart).
*    Bug fix: string-based dates in guides were not being parsed properly if they contained only numbers.


## 3.17.3

*    Bug fix: label position of columns with graph.negativeBase not equal to valueAxis.baseValue was wrong in some cases.
*    Bug fix: Value balloons of ChartCursor were displayed even if the value was out of plot area and this didn’t look right.
*    Bug fix: some issues fixed with ChartCursor property leaveCursor set to true.
*    Bug fix: Legend marker was not dashed if columns had dashed outlines and useGraphSettings was set to true.
*    Bug fix: Guide without toValue was not displaying roll-over balloon.
*    Bug fix: Stock chart’s scrollbar was not using the same font as all the panels used.
*    You can now translate am/pm strings (used when formatting time). To do this, add "am":"translatedAM", "pm":"translatedPM" to your lang 		file.
*    zeroGridAlpha property added to ValueAxis. Allows to set specific opacity for zero grid line (you can hide it at all if you set it to 			0).


## 3.17.2

*    Bug fix: step line graph with minPeriod set to MM (month) was not drawn properly.
*    Bug fix: Stock event with triangleLeft bullet produced JavaScript error.
*    Bug fix: If showEventsOnComparedGraphs was set to true (StockGraph property), events were shown on all panels instead of one.
*    Bug fix: Responsive plugin and IE11 could result JS error in some cases.


## 3.17.1

*    Bug fix: ChartCursor was not working if autoResize was set to false (since 3.16.0 version only)
*    Problems with minPeriod="fff" and Stock chart fixed.


## 3.17.0

*    widthField property added to CategoryAxis. You can specify relative width for your columns using this field and produce Mekko chart 			using this new feature (demo coming)
*    You can add listeners to chart using listeners property not only via JSON config, but directly on a chart object, like: chart.listeners 		= [{event:"dataUpdated", method:handleDataUpdate}]
*    gradientRotation property added to AmLegend. Works only with custom legend data.
*    Bug fix: if Gantt chat had more categories than colors in chart.colors array, random color was chosen for each segment instead of each 		category.
*    Bug fix: it was not possible to change graph color dynamically (since previous version only).
*    P.S. Most of the big changes in this version were made for maps, not charts.


## 3.16.0

*    Charts now use SVG icons for scrollbar, zoom-out and others (IE8 keep using PNG). This makes icons look good on retina displays on all 		resolutions. New AmChart property svgIcons with default value true was created. If you want PNG icons to be used all the time, set 			this property to false.
*    Default value of zoomOutButtonImage of AmRectangularChart changed to lens. If svgIcons is set to true (default) .svg will be added to 			the file name if SVG is supported by the browser, otherwise – .png.
*    Chart behavior on touch events improved.
*    tapToActivate property added to AmChart, with default value true. This is our new approach to solve issues with scrolling of a page on 		touch devices. Charts which require gestures like swipe (charts with scrollbar/cursor) or pinch (maps) used to prevent regular page 		scrolling and could result page to stick to the same spot if the chart occupied whole screen. Now, in order these gestures to start 		working user has to touch the chart/maps once. Regular touch events like touching on the bar/slice/map area do not require the first 			tap and will show balloons and perform other tasks as usual. If you have a map or chart which occupies full screen and your page 			does not require scrolling, set tapToActivate to false – this will bring old behavior back.
*    leaveAfterTouch property added to ChartCursor and ChartCursorSettings with default value true. This makes cursor and balloons to remain 		after user touches the chart.
*    We changed default value of fixedPosition of AmBalloon to true. We think this brings a better usability for touch devices. This results 		roll-over balloon to point to a fixed position of a slice/column/bullet instead of following the mouse. Note, AmMap overrides 				fixedPosition to false, as countries are of a irregular shape and it’s quite often that middle point of a country is outside the 			country itself.
*    showBullet property added to StockEvent, with default value false. If you set it to true, the data point will display both event and 			regular (if set) bullet.
*    recalculateValue added to StockGraph. Possible values are Open, Close, High, Low, Average and Sum. There is no default value set – 			graph uses it’s periodValue when calculating changes. For example, the graph’s periodValue is Close. This means that when data is 			grouped to longer periods (months for example) when recalculating, the graph will use Close value of the first period of the 				selection as base value and will compare each months Close value to it. If you set recalculateValue to Open, the first value of a 			month will be used as base value.
*    Second attribute, skipEvents added to validateNow method of AmStockChart.
*    autoDisplay property added to AmChart with default value false. If you set it to true the chart will automatically monitor changes of 			display style of chart’s container (or any of it’s parents) and will render chart correctly if it is changed from none to block. We 		recommend setting it to true if you change this style at a run time, as it affects performance a bit.
*    Bug fix: roll-over balloon could hide under legend if legend position was right or left.
*    Bug fix: if chart has more graphs than colors in colors array of a chart, graph’s color was chosen automatically. The problem was that 		this color was chose each time user hid/showed the graph.
*    Bug fix: setting font sizes using CSS not worked properly in some cases.
*    Bug fix: chart’s title ignored bold = false setting and always showed bold title.


## 3.15.2

*    Bug in new Microsoft Edge browser caused category labels and some other texts to disappear. The problem was fixed and the bug reported.
*    Bug fix: Gantt chart used to zoom to wrong dates if minimum/maximum was set.
*    Bug fix: Data labels were not being placed correctly for column charts with reversed value axis.
*    includeAllValues property added to ValueAxis. If you set it to true, minimum and maximum of value axis will not change while zooming/scrolling.


## 3.15.1

*    New feature which allowed to add listeners in JSON config was not working properly in some cases.
*    centerLabels property added to AxisBase. It always force-centers labels of date-based axis (equalSpacing must not be set to true).
*    Radar chart’s fills were drawn incorrectly if connect was set to false and some data was missing.
*    Pie chart could move a pixel back and forward when data was validated and chart redrawn.
*    Using fields for graph of Gantt chart was not always working properly.
*    Wrapping function improved.


## 3.15.0

*    Trend lines now support images. You can have image on both end and start of a trend line. It can be GIF, PNG or SVG (SVG won’t be visible on IE8) images. initialImage and finalImage properties and Image class were added to support this feature.
*    Annotation capabilities of the Export plugin were dramatically enhanced with the ability to add text, shapes, lines and arrows, as well as changing of opacity of items. More info.
    You can add event listeners in JSON chart config now, for example:
    “chartCursor”:{
    “listeners”:[{“event”:”changed”, “method”:handleCursorChange},{“event”:”onHideCursor”, “method”:handleCursorHide}]
    }
*    categoryBalloonText property with default value [[category]] added to ChartCursor. You can have [[toCategory]] tag in there and show category ranges this way.
*    autoWrap now works with vertical CategoryAxis. You should set chart.autoMargins = false or categoryAxis.ignoreAxisWidth = true in order this to work. You might also need to adjust margin to give labels some space.
*    labelRotation, autoRotateCount and autoRotateAngle now work with ValueAxis (when chart is rotated).
*    titleRotation property added to AxisBase. Sets rotation angle of the axis title.
*    autoWrap now works with date-based category axes.
*    onePanelOnly property added to ChartCursorSettings. If you set it to true, Stock Chart will display cursor and value balloons on currently hovered panel only.
*    top and bottom options added to showBalloonAt property of AmGraph. Balloon will be glued to the top/bottom of plot area if you set one of these.
*    pointPosition property added to ValueAxis, default value is “axis”. Alternative value is “middle”. Works with radar charts only. If you set it to “middle”, labels and data points will be placed in the middle between axes. (demo coming)
*    showZeroSlices property added to AmSlicedChart. Default value is false. If you set it to true, the chart will display outlines (if visible) and labels for slices even if their value is 0.
*    “AbsHigh” option added for periodValue property of StockGraph. When data is grouped to longer periods, the graph will show highest absolute value (positive or negative).
*    compareGraph property added to StockGraph. This allows you to set any of AmGraph properties on compared graphs instead of using old-style properties like compareGraphBulletBorderThickness. For example:
    stockGraph.compareGraph = {“bulletBorderThickness”:2, “lineAlpha”:0.4}.
*    If you change graph’s line color using lineColorField, balloon now respects this color and adjusts it’s fill or border color.
*    Title of a chart now auto-wraps if container size is smaller than title itself.
*    Mouse position detection mechanism updated. It is now compatible with CSS3 translate transform (rotation is not yet solved).
*    Radar chart supports date-based data now.
*    Compared graphs of Stock charts ids used to be unpredictable, now they are formed like this: “comparedGraph_” + stockGraph.id + “_” + dataSet.id
*    Bug fix: word-wrapping problems fixed.
*    Bug fix: pie chart with non-default startAngle could not solve label overlapping in some cases.
*    Bug fix: 3D pie chart with startAngle = 270 was placing slices at incorrect z-indices.
*    Bug fix: Stock chart’s grouping to periods with alwaysGroup set to true was not working properly in some cases.
*    Bug fix: the chart could be rendered incorrectly if display style of a container div changed from “none” to “block”
*    Bug fix: legend was missing space between entries and right border.
*    Bug fix: stacked graphs of radar chart were filled to the chart center instead of the graph.
*    Bug fix: radar chart’s axis title was not positioned properly.
*    Bug fix: pie chart’s labels could get under slices in some cases.
*    Bug fix: minimumDate and maximumDate properties of ValueAxis did not accepted dates as strings, even if chart.dataDateFormat was set.
*    Bug fix: 3D pie with big depth3D was not rendered correctly.
*    Bug fix: null values were converted to 0 when parsing data.


## 3.14.5

*    oppositeAxis property added to ChartScrollbar, with default value true. By default, scrollbar is in the opposite side of plot area from the axis. If you set this property to false, scrollbar will be placed next to category/value axis. However it won’t adjust it’s position to accommodate axis labels, so you might need to use offset property to move scrollbar away from the labels.
*    columnWidthField added to AmGanttChart. Allows to specify individual column width for each segment.
*    disableMouseEvents with default value true added to AmBalloon. Helpful in case you have fixed balloon position with some links in the balloon. You should set value of this property to false in order for links in the balloon to be clickable.
*    minorTickLength added to AxisBase. Allows to set length of ticks for minor grid lines (if they are enabled).
*    segmentData added to AmGraph. Works with AmGanttChart only and holds reference to original segment object from data provider.
*    rollOverBand, rollOutBand and clickBand events added to GaugeAxis.
*    url property added to GaugeBand.
*    Bug fix: margins of XY chart were not updated after chart.validateData() call.


## 3.14.3

*    Chart automatically detects path (chart.path variable) to images and other files if amcharts.js or ammap.js file is included as 
		`<script>` in the document source.
*    Bug fix: click on columns.bullet was not registered if valueLineEnabled was set to true on ChartCursor.
*    Bug fix: chart scrollbar could be messed up if graph.baseValue was set.


## 3.14.2

*    autoResize property added to AmChart and AmStockChart to stop the chart from resizing whenever it’s parent container size changes.
*    path property added to AmChart and AmStockChart. We recommend using this property instead of pathToImages.
*    IMPORTANT: path property, if set will also be pre-pended to non-absolute pattern URLs. This may change the behavior if you use patterns (directly in chart config or theme) with URLs that do not start with protocol or slash)
*    Bug fix: AmCharts.clear() method was not working properly with more than one chart on page.


## 3.14.1

*   Code cleanup and performance tuning.
*   Export plugin updated.
*   adjustPrecision property added to AmPieChart (default is false). Sometimes, because of a rounding, percent of a sum of all slices is not equal to 100%. If you set this to true, when this case happens, number of decimals will be increased so that sum would become 100%.


## 3.13.0

Change log will be available soon. We made a lot of nice features, including plugin which makes chars fully responsive. Meanwhile take a look at this [SVG filters demo](http://www.amcharts.com/demos/using-svg-filters/)!

## 3.12.0

*   The main new feature is that every element of a chart can have class name assigned to it – you must set **addClassNames** property of a chart to **true**. This gives a bunch of new possibilities like controlling the look using CSS, CSS animations and more. Full [list of classNames](http://www.amcharts.com/tutorials/css-class-names/).
*   **classNamePrefix** added to [AmChart](http://docs.amcharts.com/3/javascriptcharts/AmChart) and [AmStockChart](http://docs.amcharts.com/3/javascriptstockchart/AmStockChart), with default value **amcharts**. This prefix is added to all class names which are added to all visual elements of a chart in case **addClassNames** is set to true.
*   **gapField** property added to [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph). You can force graph to show gap at a desired data point using this feature, for example, if you set **graph.gapField = “gap”** and then add gap:true in one of your data items in data provider, graph will display a gap at this point.
*   **gapPeriod** property added to [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph), with default value 1.1. Using this property you can specify when graph should display gap – if the time difference between data points is bigger than duration of **minPeriod * gapPeriod**, and **connect** property of a graph is set to **false**, graph will display gap.
*   **totalTextOffset** property added to ValueAxis, with default value 0. It specifies distance from data point to total text (used with stacked graphs).
*   **compareGraphLineColor** added to [StockGraph](http://docs.amcharts.com/3/javascriptstockchart/StockGraph).
*   Bug fix: gauge axis labels could display big floating numbers in some cases.
*   Bug fix: **showStockEvents** and **hideStockEvents** used to hide all bullets, not only events.

## 3.11.3

*   Scrolling/zooming on touch devices now works a lot better.
*   Bug fix: fills of step graphs (if color changed in the middle of a graph) were not properly drawn.
*   Bug fix: period values in the legend could add one extra data item in some cases.
*   Some problems with **useUTC** set to true fixed.
*   Bug fix: adding and removing chart with mouse wheel properties enabled could result memory leak.
*   Bug fix: **fixedColumnWith** was not working properly.

## 3.11.2

*   We made quite a lot of changes regarding labels next to data points. Because of that you might require to adjust some properties after the upgrade.  New properties were introduced ([AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph) class): **labelRotation**, **labelAnchor** and **labelOffset**. These properties will help you to adjust label position in practically any way you need.
*   **fixedColumnWidth** property added to [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph). Columns will use value specified for column width and columns won’t adjust size according to the available space.
*   **treatZeroAs** property added to [ValueAxis](http://docs.amcharts.com/3/javascriptcharts/ValueAxis). It can be used with logarithmic scale axis. The fact is that 0 value can not be plotted on logarithmic axis (it’s mathematically impossible). However a lot of people were asking for solution. That’s why we added this property. For example, if you set **<span style="color: #cc6600;">treatZeroAs</span>** to 1,  all the values equal to 0 will be treated as 1 and the chart will render even if you have 0 values in your data.
*   **stepDirection** added to [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph), with default value **“right”**. You can set it to **“left”** or **“center”**. It defines to which direction step line graph should draw the step.
*   Bug fix: Funnel chart with very small slices could produce JS error.
*   Bug fix: Funnel chart with labels disabled could produce JS error.
*   Bug fix: if a page had base href set, and url of a page contained # symbol, gradients were not rendered correctly.
*   Bug fix: zooming XY chart with chart cursor could zoom-in to a wrong position.

## 3.11.1

*   **AmCharts.addInitHandler(handler,  [types])** method added to AmCharts.  **handler** is a method which will be called before initializing the chart. **types** is array of strings, specifying which chart types should call this method. If you don’t set any type, all the charts will call this method.  When handler method is called, chart instance is passed as an attribute.  You can use this feature to preprocess chart data or do some other things you need before initializing the chart.
*   Bug fix: cursor zooming of Stock chart with **equalSpacing** set to true could behave incorrectly.
*   Bug fix: columns with rounded corners were displayed incorrectly on IE8 and older (since 3.11.0 only).
*   Bug fix:  JS error occurred if GaugeAxis radius was set in pixels instead of percent.

## 3.11.0

*   **valueLineEnabled** property added to [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor) and [ChartCursorSettings](http://docs.amcharts.com/3/javascriptstockchart/ChartCursorSettings). If you set it to true, horizontal (or vertical if chart is rotated) will be displayed at a mouse position. This works only with Serial charts. Check [demo](http://www.amcharts.com/demos/multiple-panels/).
*   **valueLineBalloonEnabled** added to [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor) and [ChartCursorSettings](http://docs.amcharts.com/3/javascriptstockchart/ChartCursorSettings). If you set it to true, balloon with axis value will be displayed at a mouse position. This works only with Serial
*   charts. Check [demo](http://www.amcharts.com/demos/multiple-panels/).
*   **valueLineBalloonAxis** added to [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor). Is useful if you have more than one value axis and want to specify which axis should display value line balloon.
*   **depth3D** and **angle** properties added to Funnel chart. Allows making funnels 3D. Check [demo](http://www.amcharts.com/demos/3d-funnel-chart/).
*   **topRadius** property added to [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph). Works if **depth3D** and **angle** are bigger than 0. If you set topRadius to 1, the chart will display cylinders. In case you’ll set it to 0 – cones. Check [demo](http://www.amcharts.com/demos/3d-cylinder-chart/).
*   **showOnAxis** property added to [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph). It can only be used together with **topRadius** (when columns look like cylinders). If you set it to true, the cylinder will be lowered down so that the center of it’s bottom circle would be right on category axis. Check [demo](http://www.amcharts.com/demos/cylinder-gauge/).

## 3.10.4

*   We were so happy with proCandlesticks feature that we didn’t notice that we made it wrong – empty candles should be displayed when current close is bigger than current open. Fixed the problem in this version.

## 3.10.3

*   New property: **proCandlesticks** added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph). If this is set to true, candlesticks will be colored in a different manner – if current close is less than current open, the candlestick will be empty, otherwise – filled with color. If previous close is less than current close, the candlestick will use positive color, otherwise – negative color.
*   New property: **usePrefixes** added to [GaugeAxis](http://docs.amcharts.com/3/javascriptcharts/GaugeAxis).
*   Improvement: If stock chart’s graph has **valueField** set which was not defined in **fieldMappings**, this graph is not displayed in the legend.
*   Bug fix: if **clustered** was set to false, the graph was hidden if only this graph was visible, also the graph did not took full width if more than one clustered graphs where on the same chart.
*   Bug fix: memory leak after **validateNow()** call fixed.
*   Bug fix: **clickSlice** was fired when unhiding slice via legend marker.
*   Bug fix: Stock charts period button was deselected if data set was selected for comparing or a different data set was selected.
*   Bug fix: scrollbar could act strange in some cases (especially if **equalSpacing** was set to **true** or with non date-based data).
*   Bug fix: if **AmCharts.useUTC** was set to **true**, chart was not parsing date strings correctly.
*   Bug fix: Stock chart’s scrollbar did not apply language if not default was used.
*   Bug fix: if multiple charts on the same page used different languages, [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor) balloon used language of the last chart.
*   Bug fix: if custom **urlTarget** was set for a chart, chart kept opening new window instead of opening url in the same one.
*   Bug fix: if **graphBulletSize** was set to 1 on [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor), **graphBulletAlpha** property was ignored.

## 3.10.2

*   Skipped this version

## 3.10.1

*   Bug fix: if a column graph had **newStack** property set to **true** and the value of this graph was missing, the next graphs were stacked in a wrong position.
*   Bug fix: In case multiple value axes chart had line graphs with **connect** set to **false** and there were gaps in the data, gaps might not be displayed.
*   Value axis labels with **logarithmic** set to **true** could use wrong interval in some cases.

## 3.10.0

*   **fillToAxis** property added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph). It can only be used with [AmXYCharts](http://docs.amcharts.com/3/javascriptcharts/AmXYChart). If you set this property to id or reference of your X or Y axis, and the **fillAlphas** is &gt; 0, the area between graph and axis will be filled with color, like in [this demo](http://www.amcharts.com/demos/xy-chart-fills-axis/).
*   **showAt** property added to [StockEvent](http://docs.amcharts.com/3/javascriptstockchart/StockEvent). It will allow you to place bullets at **open**, **close**, **low** or **high** values (mostly used with candlestick/ohlc graphs)
*   **value** property added to [StockEvent](http://docs.amcharts.com/3/javascriptstockchart/StockEvent). It will allow you positioning stock event bullets at any value you want.
*   **useNegativeColorIfDown** property added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph). If **negativeLineColor** and/or **negativeFillColors** are set and **useNegativeColorIfDown** is set to true (default is false), the **line**, **step** and **column** graphs will use these colors for lines, bullets or columns if previous value is bigger than current value. In case you set **openField** for the graph, the graph will compare current value with **openField** value instead of comparing to previous value. Here [is a demo](http://www.amcharts.com/demos/line-different-colors-ups-downs/).
*   **expand** property added to [Guide](http://docs.amcharts.com/3/javascriptcharts/Guide). Works if a guide is added to [CategoryAxis ](http://docs.amcharts.com/3/javascriptcharts/CategoryAxis)and this axis is non-date-based. If you set it to true, the guide will start (or be placed, if it’s not a fill) on the beginning of the **category** cell and will end at the end of **toCategory** cell.
*   **balloonText** property added to [GaugeBand](http://docs.amcharts.com/3/javascriptcharts/GaugeBand). When rolled-over, band will display balloon if you set some text for this property.
*   **labelFunction** property added to [AmSlicedChart ](http://docs.amcharts.com/3/javascriptcharts/AmSlicedChart)(applies for [AmPieChart ](http://docs.amcharts.com/3/javascriptcharts/AmPieChart)and [AmFunnelChart](http://docs.amcharts.com/3/javascriptcharts/AmFunnelChart)). You can use it to format data labels in any way you want.
*   **clearSelection()** method added to [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor). Can be used when **selectWithoutZooming** is set to true and you need to clear the selection made by user.
*   **labelOffset** property added to [AxisBase](http://docs.amcharts.com/3/javascriptcharts/AxisBase). You can use it to adjust position of axes labels. Works both with [CategoryAxis ](http://docs.amcharts.com/3/javascriptcharts/CategoryAxis)and [ValueAxis](http://docs.amcharts.com/3/javascriptcharts/ValueAxis).
*   **switchable** property added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph), with default value set to true. If you set it to false, the graph will not be hidden when user clicks on legend entry.
*   **valueFunction** added to [AmLegend](http://docs.amcharts.com/3/javascriptcharts/AmLegend). You can use it to format value labels in any way you want.
*   **tickPosition** property added to [CategoryAxis](http://docs.amcharts.com/3/javascriptcharts/CategoryAxis). It can be set to **middle** (default) or **start**. Works only with non-date-based data.  [Demo ](http://www.amcharts.com/demos/simple-column-chart/#theme-patterns)of **tickPosition** set to **start**.
*   **labelFunction** added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph). You can use it to format labels of data items in any way you want.
*   Pattern objects can have **color** property now. If your pattern is transparent, the background will be filled with this **color**, like in [this example](http://www.amcharts.com/demos/map-with-patterns/).
*   **graphBulletAlpha** added to [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor). If you make graph’s bullets invisible by setting their opacity to 0 and will set **graphBulletAlpha** to 1, the bullets will only appear at the cursor’s position. Here is a [demo illustrating this](http://www.amcharts.com/demos/step-line-chart/).
*   **labelColorField** added to [CategoryAxis](http://docs.amcharts.com/3/javascriptcharts/CategoryAxis). You can use it to set color of a axis label. Works only with non-date-based data.
*   **maxLabelWidth** added to [AmSlicedChart ](http://docs.amcharts.com/3/javascriptcharts/AmSlicedChart)(applies for [AmPieChart ](http://docs.amcharts.com/3/javascriptcharts/AmPieChart)and [AmFunnelChart](http://docs.amcharts.com/3/javascriptcharts/AmFunnelChart)). If width of the label is bigger than **maxLabelWidth**, it will be wrapped.
*   **labelWidth** property added to [AmLegend](http://docs.amcharts.com/3/javascriptcharts/AmLegend). If width of the label is bigger than **labelWidth**, it will be wrapped.
*   **compareGraphBulletColor** property added to [StockGraph](http://docs.amcharts.com/3/javascriptstockchart/StockGraph).
*   **mouseWheelZoomEnabled** added to [AmSerialChart](http://docs.amcharts.com/3/javascriptcharts/AmSerialChart). Specifies if zooming of a chart with mouse wheel is enabled. If you press shift while rotating mouse wheel, the chart will scroll.
*   **boldLabels** added to [AxisBase](http://docs.amcharts.com/3/javascriptcharts/AxisBase). Labels will be bold if you set it to true.
*   Bug fix: balloons no longer flicker if mouse is moved fast on column charts.
*   Bug fix: **minSelectedTime** and **maxSelectedTime** was not working properly on [AmStockChart](http://docs.amcharts.com/3/javascriptstockchart/AmStockChart).
*   Bug fix: position of data labels in 3D stacked columns was not always accurate.
*   Bug fix: value balloons of [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor) were overlapping if the chart was rotated.
*   Bug fix: if a div containing chart/map had CSS3 transformations applied, the mouse position was calculated incorrectly.
*   Bug fix: **addGuide** method was not working on IE borwsers.
*   Bug fix: Safari could leave previously rendered chart or other objects in the background after the chart was redrawn (only since 3.9.0).

## 3.9.1

*   Bug fix: Stock chart was not working properly with millisecond data.
*   Bug fix: if all graphs of XY chart were hidden from the legend, the chart could start acting weird.
*   Bug fix: sometimes the graph’s balloon became invisible if graph was hidden/unhidden from the legend.
*   Bug fix: angular gauge was not working properly with negative values.
*   Bug fix: if **equalSpacing** was set to **true**, the zooming with chart cursor could zoom-in to a wrong position (Stock chart only).
*   Bug fix: cursors of stock chart could get out of sync in some cases.

## 3.9.0

*   We jumped directly to V 3.9.0 from 3.4.9 in order to keep the same version numbers for charts and maps, as they are often used together. This will help to avoid some misunderstandings.
*   Serious memory leak fixed. It appeared on when chart was redrawn. We noticed this with recent version of Chrome and it seems like this is browser problem. Nevertheless, we found a solution. We strongly recommend to update to this version if you refresh chart with a new data or rebuild it a lot for some other reasons.
*   A possibility to switch languages easily added. Now you can easily change language of a chart (there are not too many texts there, most of them are names of months and weekdays, but still). To do this, you must include lang file from amcharts/lang/ folder and set **chart.language = “de”** or some other language.
*   Exporting chart as SVG now produces one nice file (used to produce separate files for legend and a chart)
*   balloonPointerOrientation added to [ChartCursor ](http://docs.amcharts.com/3/javascriptcharts/ChartCursor)class (also for [ChartCursorSettings](http://docs.amcharts.com/3/javascriptstockchart/ChartCursorSettings)).

## 3.4.10

*   Fix: Saving chart as image was not working properly with IE11 since last release.
*   **recalculateFromDate** property added to [StockPanel](http://docs.amcharts.com/3/javascriptstockchart/StockPanel), allows you to set the date since when the values should be recalculated to percent.
*   Fix: sometimes, when data of StockChart was recalculated to percent, the recalculation started a bit too early which made 0 value to be outside the selection.
*   Fix: new way of using **amExport** was not working properly on [StockChart](http://docs.amcharts.com/3/javascriptstockchart/AmStockChart).

## 3.4.9

*   **clickItem**, **rollOverItem** and **rollOutItem** events added to [AxisBase](http://docs.amcharts.com/3/javascriptcharts/AxisBase). This will allow you to register mouse events on both [CategoryAxis ](http://docs.amcharts.com/3/javascriptcharts/CategoryAxis)and [ValueAxis ](http://docs.amcharts.com/3/javascriptcharts/ValueAxis)labels.
*   Fix: Stock Chart used not to show the beginning or the end of period if the data was grouped but the actual data started/ended somewhere in the middle of this period. This could cause some confusions. Now it is fixed, however if you prefer old behaviour, set **chart.extendToFullPeriod = false;**
*   We added a more easy way to use exporting as an image feature. Charts has **amExport** property now and here is an [AmExport ](http://docs.amcharts.com/3/javascriptcharts/AmExport)class reference.

## 3.4.8

*   **guides** property added to [AmCoordinateChart](http://docs.amcharts.com/3/javascriptcharts/AmCoordinateChart). Instead of adding guides to the axes, you can add them using this property.
*   **showComparedOnTop** property added to [StockPanel](http://docs.amcharts.com/3/javascriptstockchart/AmStockChart). This allows you to set the order of main graph vs compared ones. Default value is **true**.
*   Bug fix: **textAlign **property of [AmBalloon ](http://docs.amcharts.com/3/javascriptcharts/AmBalloon)was not working properly.
*   Bug fix: [GaugeAxis ](http://docs.amcharts.com/3/javascriptstockchart/GaugeAxis)bands might me displayed incorrectly if axis started not on 0 value.
*   Bug fix: if panning was enabled for stock chart, different panels could get out of sync in some cases.
*   Bug fix: if **startAngle** was set for [AmPieChart](http://docs.amcharts.com/3/javascriptcharts/AmPieChart), labels could be displayed at a wrong position.

## 3.4.7

*   You no longer need to add empty data items for dates if you want to show gaps in your data, it’s enough to set **connect** property of [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph) to false.
*   Instead of **numberFormatter** and **percentFormatter** properties of [AmChart](http://docs.amcharts.com/3/javascriptcharts/AmChart) we recommend using separate properties – **precision**, **percentPrecision**, **decimalSeparator** and **thousandsSeparator**. [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph) class also has **precision** property in case you need a separate precision for a graph. The old formatters will still work.
*   **minBulletSize** property of [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph) default changed to 3, as since the 3.4.4 due new way of bullet size calculation, the bubble with the most small value might not be seen at all.
*   Bug fix: Stock chart could freeze when panning it (only if **pan** for cursor was set to true).
*   Bug fix: **alphaField** was ignored by pie chart.
*   Bug fix: [PeriodSelector](http://docs.amcharts.com/3/javascriptstockchart/PeriodSelector) of Stock chart use to select some extra days when predefined period of several years/months was selected.

## 3.4.6

*   **fullWidth** property added to [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor). If set to **true**, instead of a cursor line user will see a fill which width will always be equal to the width of one data item. We’d recommend setting **cusrsorAlpha** to 0.1 or some other small number if using this feature. [Demo of the feature](http://www.amcharts.com/demos/duration-on-value-axis/).
*   **twoLineMode** property added to [CategoryAxis](http://docs.amcharts.com/3/javascriptcharts/CategoryAxis) and [CategoryAxesSettings](http://docs.amcharts.com/3/javascriptstockchart/CategoryAxesSettings). It works only when **parseDates** is set to true and **equalSpacing** is false. If you set it to true, at the position where bigger period changes, category axis will display date strings of bot small and big period, in two rows.
*   **line** marker type is again available for [AmLegend](http://docs.amcharts.com/3/javascriptstockchart/AmLegend)‘s **markerType** property (also markerType of [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph) if you need to set custom types for your graphs).
*   [GaugeAxis](http://docs.amcharts.com/3/javascriptcharts/GaugeAxis) properties **valueInterval** and **minorTickInterval** doesn’t have default values since this version, as it might cause problems with big numbers. Instead we added **gridCount** property which is 5 by default. Note, [GaugeAxis](http://docs.amcharts.com/3/javascriptcharts/GaugeAxis) doesn’t adjust **gridCount**, so you should check your values and choose a proper **gridCount** which would result grids at round numbers.

## 3.4.5

*   **newStack** property added to **AmGraph**. If you set it to true, column chart will begin new stack. This allows having [Clustered and Stacked column/bar](http://www.amcharts.com/demos/stacked-clustered-column-chart/) chart.
*   Bug fix: since  3.4.4 old IE browsers failed to display chart if legend position was **left** or **right**<span style="line-height: 1.428571429;"> </span>

## 3.4.4

*   You can set **divId** for [StockLegend ](http://docs.amcharts.com/3/javascriptstockchart/StockLegend)now too. This should be id or reference to a div outside the chart where you want a legend  to appear.
*   Adjusted algorithm of bullet size calculation for Bubble (XY) chart.
*   **showBulletsAt** property added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph). Works with **candlestick** graph type, you can set it to **open**, **close**, **high**, **low**. If you set it to **high**, the events will be shown at the tip of the high line.
*   New property, **minDistance** added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph). Default value is 1. It is useful if you have really lots of data points. Based on this property the graph will omit some of the lines (if the distance between points is less that **minDistance**, in pixels). This will  not affect the bullets or indicator in anyway, so the user will not see any difference (unless you set minValue to a bigger value, let say 5), but will increase performance as less lines will be drawn. By setting value to a bigger number you can also make your lines look less jagged.
*   Changed default value of panEventsEnabled (property of [AmChart ](http://docs.amcharts.com/3/javascriptcharts/AmChart)and [PanelsSettings ](http://docs.amcharts.com/3/javascriptstockchart/PanelsSettings)classes) **from** false to **true**.
*   Bug fix: right scrollbar grip of Stock chart was not working properly with **equalSpacing** set to true and **minPeriod** was not **DD** (since 3.4.3 version only).
*   Bug fix: if amcharts.js and ammap.js was included for several times (you shouldn’t do that, but still), the charts were not working properly.
*   Bug fix: if the slice of a pie/funnel was hidden and the method rollOverSlice(slice) was called from outside, the balloon was still shown.
*   Bug fix: Sometimes part of a legend was cut-off when labels were long enough and legend position was **left** or **right.**
*   Bug fix: outline of funnel chart slices had some extra unnecessary lines.

## 3.4.3

*   **processDelay** property added to AmCharts class. If you set **AmCharts.processDelay = 200;** all the charts on the page will be rendered with 200 ms intervals. This is very comfortable if you have a lot of charts on the page and do not want to overload the device CPU. </span>
*   A third parameter, **delay** was added to **AmCharts.makeChart** method. It specifies the delay in ms, at which the chart must be rendered, for example: **AmCharts.makeChart(“chartDiv”, {chart config}, 200);**</span>
*   **offset** property added to ChartScrollbar. Allows to place scrollbar apart from plot area.
*   **autoRotateCount** and **autoRotateAngle** properties added to CategoryAxis. Works only when dates are not parsed. Axis labelsl will be rotated if the number of series will be equal or exceed **autoRotateCount** value.
*   **rollOverGraph** and **rollOutGraph** events added to AmCoordinateChart.
*   **changed** event of stock chart’s period selector passes the original mouse event as event property.
*   Bug fix: Stock chart used to select one extra period when dates were entered in input fields and **equalSpacing** was set to true;
*   Bug fix: some issues with floating point errors fixed
*   Bug fix: zoom-out button border was always visible on IE8.
*   Bug fix: funnel chart was not working properly with labels disabled.
*   filesaver.js was updated so that in case it is included with IE8 and older browsers, it wouldn’t throw JS error.

## 3.4.2

*   Bug fix: if pie slice had no label, the external method **rollOverSlice(index)** was not working
*   Bug fix: x switch of the legend position adjusted
*   Bug fix: when **autoWrap** for category axis was set to **true**, in some cases axis title was cut.
*   **markPeriodChange** was set to true in [CategoryAxesSettings](http://docs.amcharts.com/3/javascriptstockchart/CategoryAxesSettings).

## 3.4.1

*   Patterns theme added.
*   Themes were updated a bit.
*   Labels of angular gauge axis adjusted.
*   When scrolling serial/stock charts with mousewheel (chart.mouseWheelScrollEnabled must be set to true), if user press shift button, the chart will zoom-in or zoom-out;
*   **adjustment** property added to  [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor). Default value is 0, if you set it to -1, the balloon will show near previous, if you set it to 1 – near next data point.

## 3.4.0

*   Link to amCharts.com site in a free version was made less noticeable – it uses chart’s font color and font size and you can adjust it’s position using **creditsPosition** property of [AmChart](http://docs.amcharts.com/3/javascriptcharts/AmChart). Possible values are: **top-left**, **top-right**, **bottom-right** and **bottom-left**. This will help you to achieve better layout of a chart.
*   We fixed typo of [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor) property – it was showNextAvalable and now is **showNextAvailable**. The old one won’t work.
*   Since now you can scroll serial and stock charts with mouse wheel. To enable this, set **chart.mouseWheelScrollEnabled = true** (default is false).
*   **moved** event added to [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor). It is dispatched every time the mouse is moved. The event object has the following properties: **x**, **y** (coordinates of the cursor), **chart** and **zooming**.
*   **axisX** and **axisY** properties added to [AxisBase](http://docs.amcharts.com/3/javascriptcharts/AxisBase). They are read-only and returns **x** and **y** positions of the axis.
*   **unit** and **unitPosition** (with possible values **left** and **right**) added to [GaugeAxis](http://docs.amcharts.com/3/javascriptcharts/GaugeAxis) class.
*   **autoWrap** property added to [CategoryAxis](http://docs.amcharts.com/3/javascriptcharts/CategoryAxis), with default value **false**. If you set it to **true**, the axis labels will be wrapped if they won’t fit in the allocated space.
*   **minHorizontalGap** (default 75) and **minVerticalGap** (35) properties added to [AxisBase](http://docs.amcharts.com/3/javascriptcharts/AxisBase). They are used to calculate the number of grid lines when **autoGridCount** is **true**. You can modify these values to have more or less grid lines.

## 3.3.6

*   Bug fix – charts with legend could fail if there was a Google Analytics script in the page.
*   **stepDirection** property added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph). If you set it to **left**, step line graph will draw the step to the left of the date/category.

## 3.3.5

*   Bug fix: 3D pie chart was not rendered in IE8 and older (since 3.3.4 version only).
*   Candlestick graphs can display patterns.
*   Old listeners are removed automatically if the same listener was added, this helps to avoid duplicate calls of event handlers.
*   Bug fix: \n in **labelText** of [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph) is now properly displayed as new line.

## 3.3.4

*   Export as image script fixed – bullets of charts with scrollbars were not exported.
*   dataContext property added to [SerialDataItem](http://docs.amcharts.com/3/javascriptcharts/SerialDataItem). It holds reference to original data object and might be used when using **labelFunction** to format custom balloon text and in some other cases.
*   XY chart can display bullets with patterns (if **valueField** is set).

## 3.3.3

*   **hideBalloonTime** property added to [AmChart](http://docs.amcharts.com/3/javascriptcharts/AmChart) class, default value is 150 (milliseconds). It sets time after which balloon is hidden if user rolls-out of the object. Increasing the time might help to prevent balloon flickering while moving the mouse over the object.
*   **useLineColorForBulletBorder** property added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph). Might help in some situations, especially when using themes.
*   3D charts now look a lot better with patterns.
*   **endWidth** property added to [GaugeArrow ](http://docs.amcharts.com/3/javascriptcharts/GaugeArrow)(default value 0). This will allow having more modern, rectangular arrows.
*   [**facePattern**](http://docs.amcharts.com/3/javascriptcharts/AmAngularGauge) property added to [AmAngularGauge](http://docs.amcharts.com/3/javascriptcharts/AmAngularGauge). You can fill gauge’s face with some pattern using it.
*   Bug fix: new lines were ignored in balloons.

## 3.3.2

*   You can now set theme for all the charts on your page by setting: **AmCharts.theme = AmCharts.themes.light;** If you are creating charts using JavaScript API, not JSON, then this is quite a comfortable way, as you won’t need to pass theme to each object you create.
*   Bug fix: **rendered** event was fired only on first render, now it is fired each time the chart is rendered after **chart.validateNow();** method is called. This bug caused the export buttons to disappear after the **validateNow()** method.
*   **showNextAvalable** property added to [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor) (default is **false**). If **true**, the graph will display balloon on next available data point if currently hovered item doesn’t have value for this graph.
*   **periodSpan** property added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph) (default is 1). This property can be used by step graphs – you can set how many periods one horizontal line should span.
*   **end** option added to **pointPosition** property of [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph).

## 3.3.1

*   Bug fix:  **\n** was replaced with **&lt;br&gt;** in category axis and the tag was displayed.
*   Bug fix: if **lineColorField** or **dashLengthField** or **fillColorsField** was set, the graph could loose the setting if zoomed.

## 3.3.0

*   Since this version our charts and maps support themes. This means that instead of setting every property for each graph or axis or any other object, you can set new defaults in a theme file. This will make developers life a lot easier. Currently you can find three themes in **amcharts/themes** folder – **dark.js**, **light.js** and **chalk.js** To set a theme for a chart, simply set theme property to the name of the file: **theme:”light”**. Note, this will work only if you are creating chart using JSON config. If you do it in old way (JSON config is supported since v 3.2.0), you should pass theme object for each new object you build, for example: **var graph = new AmCharts.AmGraph(AmCharts.themes.light);** We will be adding more themes soon. Check **\_usingThemes.html** file in samples folder to see themes in action.
*   **patterns** property added to [AmSlicedChart](http://docs.amcharts.com/3/javascriptcharts/AmSlicedChart) and [AmCoordinateChart](http://docs.amcharts.com/3/javascriptcharts/AmCoordinateChart) – instead of setting a pattern for a slice/graph, you can pass array of patterns using this property.
*   You can now control zoom-out buttons with the following new properties of [AmRectangularChart](http://docs.amcharts.com/3/javascriptcharts/AmRectangularChart): **zoomOutButtonImageSize**, **zoomOutButtonImage**, **zoomOutButtonColor**, **zoomOutButtonAlpha**, **zoomOutButtonRollOverAlpha**, **zoomOutButtonPadding**.

## 3.2.0

*   **AmCharts.makeChart(divID, chartConfig);** method added. **divID** is id of a **div** where your chart should appear. **chartConfig** is JSON object with chart configuration. Check examples with **_JSON_** prefix in samples folder to see this in action.
*   **type** property added to [AmChart](http://docs.amcharts.com/3/javascriptcharts/AmChart) class. It is required to specify type to one of the following, when creating charts from JSON config: **serial**, **xy**, **radar**, **pie**, **gauge**, **funnel**, **map**, **stock.**
*   A possibility to export charts as image/pdf/svg added for all modern browsers except IE9 (IE10 is supported). The exporting doesn’t require any server side software and is made using JavaScript libraries only. Check samples with **_exporting_** prefix to see this in action. Exporting to SVG doesn’t work very properly with stock chart or charts with legend (will offer saving multiple files).
*   You can set any legend items via **data** property of [AmLegend](http://docs.amcharts.com/3/javascriptcharts/AmLegend), for example: **legend.data = [{title:”first”, color:”#CC0000″, value:50}, {title:”second”, color:”#00CC00″, value:100}];** This allows creating any legend items you want. Call **chart.legend.validateNow();** if you change legend’s data at run time.
*   [AmAngularGauge](http://docs.amcharts.com/3/javascriptcharts/AmAngularGauge) supports legend now.
*   **gridAboveGraphs**<span style="line-height: 1.428571429;"> property added to </span>[AmCoordinateChart](http://docs.amcharts.com/3/javascriptcharts/AmCoordinateChart)<span style="line-height: 1.428571429;">. This allow to show grid lines above your graphs, as world-famous </span><span style="line-height: 1.428571429;">data visualization guru Edward Tufte suggests. Note, this won’t work properly with 3D charts.</span>
*   You can also use negative values from -90 to -1 for **labelRotation** property of [CategoryAxis](http://docs.amcharts.com/3/javascriptcharts/CategoryAxis) since now.
*   Bug fix: if a chart with scrollbar was rotated after the chart is created, the scrollbar’s graph was shifted to a wrong position.
*   Bug fix: column graph type wasn’t displayed in chart scrollbar (since 3.1.0).
*   Bug fix: step line with changing line color was rendered incorrectly if some values were missing.
*   Bug fix: **labelPosition** values **inside** and **middle** were not working properly with bar charts.
*   Bug fix: [AmAngularGauge](http://docs.amcharts.com/3/javascriptcharts/AmAngularGauge) chart wasn’t firing **rendered** event.

## 3.1.1

*   Bug fix: FireFox error messages about style declarations fixed.
*   Bug fix: **maxWidth** property of [AmBalloon](http://docs.amcharts.com/3/javascriptcharts/AmBalloon) was ignored.

## 3.1.0

*   Great new features added – charts now support patterns (can fill bars, lines and slices with images) and can simulate hand drawn charts – the lines will be a bit distorted and produce a nice effect. Check our new [inspiring samples](http://www.amcharts.com/inspiration/)  to see new possibilities in action.
*   Patterns can be set for entire graphs or for individual columns/slices. In case you want to set pattern for a graph, use **pattern** property of [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph). If you want to set individual pattern for a column or slice, describe patterns in chart’s data provider and set **patternField** for a graph or pie/funnel chart. Value of pattern should be object with **url**, **width**, **height** of an image, optionally it might have **x**, **y**, **randomX** and **randomY** values. For example: **graph.pattern = {“url”:”../amcharts/patterns/black/pattern1.png”, “width”:4, “height”:4};** check amcharts/patterns folder for some patterns. You can create your own patterns and use them. Note, **x**, **y**, **randomX** and **randomY** properties won’t work with IE8 and older.
*   <span style="line-height: 1.428571429;">if you set **chart.handDrawn = true**, the lines of a chart will be distorted and will produce hand-drawn effect. </span>You can also modify **handDrawScatter** (default value is 2) and **handDrawThickness** (default value 1)  of [AmChart](http://docs.amcharts.com/3/javascriptcharts/AmChart) values for more scattered view.
*   **offsetY** and **offsetX** properties added to [AmBalloon](http://docs.amcharts.com/3/javascriptcharts/AmBalloon). Specifies the distance from the mouse position to balloon’s pointer. You might want to increase distance when using hand drawn style.

## 3.0.0

*   <span style="line-height: 1.428571429;">As not all users require all type of charts, we spilt the js file into several files – one main **amcharts.js** file, plus </span>a separate js file for each chart type. This means you can include only the charts you need. If you are worried about number of requests, you can simply copy/paste the source of the charts you use to the main file.
*   <span style="line-height: 1.428571429;">Although we changed some default values in order to improve usability of the charts, the only thing you should worry </span>about when upgrading from v2 to v3 is the feature mention above – you should include two or more js files in order your charts to work. If you don’t like the changed defaults, you can always set them to the previous values in your chart
*   <span style="line-height: 1.428571429;">New chart type added – Funnel / Pyramid chart. </span>As this chart type has a lot of in common with pie chart, we created one base class for these chart types – [AmSlicedChart](http://docs.amcharts.com/3/javascriptcharts/AmSlicedChart). [AmPieChart](http://docs.amcharts.com/3/javascriptcharts/AmPieChart) and [AmFunnelChart](http://docs.amcharts.com/3/javascriptcharts/AmFunnelChart) now extend this class.
*   New chart type added – [AngularGauge](http://docs.amcharts.com/3/javascriptcharts/AmAngularGauge). Supports multiple axes and multiple arrows.
*   We added lots of new features to our charts and with these features you can create new chart types, like:
*   Horizontal or vertical bullet chart – bulletChart.html
*   Waterfall chart – waterFallChart.html
*   Step chart without risers – lineStepNoRisers.html
*   Error chart (both Serial and XY) – errorChart.html
*   Possibility to show minor grid for both Category and Value axis. **minorGridEnabled** (default value false) and **minorGridAlpha** (default 0.07) properties added to [AxisBase](http://docs.amcharts.com/3/javascriptcharts/AxisBase) class.
*   Possibility to change line graphs’ line/fill color on any data point to create highlighted sections of the graph. To achieve this, you should set **lineColorField** and/or **fillColorsField** for your graph and have a field in your data which would contain color values at a point where you want the graph to change it’s color.
*   Possibility to switch line from solid to dashed. Columns can also have dashed outline. To achieve this, you should set **dashLengthField** for your graph and have a field in your data which would contain dash length value at a point where you want the graph to change from solid to dashed or vice versa.
*   Date strings in data now supported. Even if your chart parses dates, you can pass them as strings in your data – all you need to do is to set data date format and the chart will parse dates to date objects. This means that now data for date-based chart can be in legit JSON format. **dataDateFormat** property added to [AmSerialChart](http://docs.amcharts.com/3/javascriptcharts/AmSerialChart) and [AmStockChart](http://docs.amcharts.com/3/javascriptstockchart/AmStockChart).
*   When moving chart cursor over the chart, hovered bullets can change their size. If a graph has bullets and you added [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor) to the chart, bullets will become bigger when char cursor is over them. **graphBulletSize** property with default value 1.7 added to [ChartCursor](http://docs.amcharts.com/3/javascriptcharts/ChartCursor). If you want to disable this feature, set the value to 1.
*   Legend can now display period value. When user is not hovering the chart, legend can show **sum**, **average**, **open**, **close**, **low** or **high** values of selected period. **periodValueText** added to [AmLegend](http://docs.amcharts.com/3/javascriptcharts/AmLegend) and **legendPeriodValueText** added to [AmGraph](http://docs.amcharts.com/3/javascriptcharts/AmGraph) to achieve this. The tags should be made out of two parts – the name of a field (value / open / close / high / low) and the value of the period you want to be show – open / close / high / low / sum / average / count. For example: **[[value.sum]]** means that sum of all data points of value field in the selected period will be displayed.
*   To achieve the same with stock chart, we added **periodValueTextRegular** and **periodValueTextComparing** proprties to [StockLegend](http://docs.amcharts.com/3/javascriptstockchart/StockLegend). To show percent period values, you should add **percent.** prefix for your tag, for example: **[[percents.value.close]]** means that last percent value of a period will be displayed.
*   Legend markers can now mirror graph’s settings, displaying a line and a real bullet as in the graph itself. **useGraphSettings** property with default value false was added to [AmLegend](http://docs.amcharts.com/3/javascriptstockchart/AmLegend). Note, we also removed **line** and **dashedLine** marker types because of this – use the **useGraphSettings** feature in case you need lines as markers in the legend.
*   Legend now supports custom markers (images). **customMarker** property was added to [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph). You should set path to the image which should be displayed in the legend.
*   Diamond bullet type added to [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph). Set **graph.bullet = “diamond”** to use it.
*   Dynamic bullet size based on value axis / Error chart. Error chart is a regular serial or XY chart with bullet type set to **errorX** or **errorY**. The graph should know which axis should be used to determine the size of this bullet – that’s when **graph.bulletAxis** property should be set. Besides that, you should also set **graph.errorField**. You can also use other bullet types with this feature too. For example, if you set **bulletAxis** for XY chart, the size of a bullet will change as you zoom the chart.
*   You can specify custom column width for each graph individually. **columnWidth** property added to [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph). Note, you set relative width here (0 – 1), not width in pixels.
*   Columns can be overlaid on other columns, without making axis as stacked. **clustered** property added to [AmGraph](http://docs.amcharts.com/3/javascriptstockchart/AmGraph). In case you want to place graph’s columns in front of other columns, set it to false.
*   Resize grips were made bigger to make life easier for users on touch devices.
*   Balloons can now display any HTML and CSS inside them. This means you can add images, format text or display just about any HTML/CSS content. Because of this new feature, we removed **textShadow** property of [AmBalloon](http://docs.amcharts.com/3/javascriptstockchart/AmBalloon) in this version.
*   Balloon now can animate from point to point and also fade out when user moves away from the chart. **animationDuration** and **fadeOutDuration** properties added to [AmBalloon](http://docs.amcharts.com/3/javascriptstockchart/AmBalloon), with default values 0.3. **animationDuration** property was also added to [ChartCursor](http://docs.amcharts.com/3/javascriptstockchart/ChartCursor), so that the cursor line would also animate to its position.
*   Balloon now can display shadow. **shadowColor** (default #000000) and **shadowAlpha** (default 0.4) added to [AmBalloon](http://docs.amcharts.com/3/javascriptstockchart/AmBalloon).
*   Some default values of [AmBalloon](http://docs.amcharts.com/3/javascriptstockchart/AmBalloon) changed for a better usability – **adjustBorderColor** to true, **cornerRadius** to 0, **pointerWidth** to 6, **color** to #000000.
*   Stock chart can display scrollbar on top of the chart – you should set position property of [ChartScrollbarSettings](http://docs.amcharts.com/3/javascriptstockchart/ChartScrollbarSettings) to **“top”**.<span style="line-height: 1.428571429;"> </span>
