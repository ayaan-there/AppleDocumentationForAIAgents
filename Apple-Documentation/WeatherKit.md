# WeatherKit Documentation

Source: https://sosumi.ai/documentation/weatherkit

---
title: WeatherKit
source: https://developer.apple.com/documentation/weatherkit
timestamp: 2026-02-13T19:04:04.786Z
---

## Fundamentals

- [Fetching weather forecasts with WeatherKit](/documentation/weatherkit/fetching_weather_forecasts_with_weatherkit)
- [Weather](/documentation/weatherkit/weather)

### Getting the forecast

- [var availability: WeatherAvailability](/documentation/weatherkit/weather/availability)
- [var currentWeather: CurrentWeather](/documentation/weatherkit/weather/currentweather)
- [var dailyForecast: Forecast<DayWeather>](/documentation/weatherkit/weather/dailyforecast)
- [var hourlyForecast: Forecast<HourWeather>](/documentation/weatherkit/weather/hourlyforecast)
- [var minuteForecast: Forecast<MinuteWeather>?](/documentation/weatherkit/weather/minuteforecast)

### Getting weather alerts

- [var weatherAlerts: [WeatherAlert]?](/documentation/weatherkit/weather/weatheralerts)
- [WeatherService](/documentation/weatherkit/weatherservice)

### Creating the object

- [convenience init()](/documentation/weatherkit/weatherservice/init())

### Obtaining forecasts

- [func weather(for: CLLocation) async throws -> Weather](/documentation/weatherkit/weatherservice/weather(for:))
- [func weather<T1, T2>(for: CLLocation, including: WeatherQuery<T1>, WeatherQuery<T2>) async throws -> (T1, T2)](/documentation/weatherkit/weatherservice/weather(for:including:_:))
- [func weather<T1, T2, T3>(for: CLLocation, including: WeatherQuery<T1>, WeatherQuery<T2>, WeatherQuery<T3>) async throws -> (T1, T2, T3)](/documentation/weatherkit/weatherservice/weather(for:including:_:_:))
- [func weather<T1, T2, T3, T4>(for: CLLocation, including: WeatherQuery<T1>, WeatherQuery<T2>, WeatherQuery<T3>, WeatherQuery<T4>) async throws -> (T1, T2, T3, T4)](/documentation/weatherkit/weatherservice/weather(for:including:_:_:_:))
- [func weather<T1, T2, T3, T4, T5>(for: CLLocation, including: WeatherQuery<T1>, WeatherQuery<T2>, WeatherQuery<T3>, WeatherQuery<T4>, WeatherQuery<T5>) async throws -> (T1, T2, T3, T4, T5)](/documentation/weatherkit/weatherservice/weather(for:including:_:_:_:_:))
- [func weather<T1, T2, T3, T4, T5, T6>(for: CLLocation, including: WeatherQuery<T1>, WeatherQuery<T2>, WeatherQuery<T3>, WeatherQuery<T4>, WeatherQuery<T5>, WeatherQuery<T6>) async throws -> (T1, T2, T3, T4, T5, T6)](/documentation/weatherkit/weatherservice/weather(for:including:_:_:_:_:_:))
- [static let shared: WeatherService](/documentation/weatherkit/weatherservice/shared)

### Providing attribution

- [var attribution: WeatherAttribution](/documentation/weatherkit/weatherservice/attribution)

### Instance Methods

- [func dailyStatistics<each T>(for: CLLocation, forDaysIn: DateInterval, including: repeat DailyWeatherStatisticsQuery<each T>) async throws -> (repeat DailyWeatherStatistics<each T>)](/documentation/weatherkit/weatherservice/dailystatistics(for:fordaysin:including:))
- [func dailyStatistics<each T>(for: CLLocation, including: repeat DailyWeatherStatisticsQuery<each T>) async throws -> (repeat DailyWeatherStatistics<each T>)](/documentation/weatherkit/weatherservice/dailystatistics(for:including:))
- [func dailyStatistics<each T>(for: CLLocation, startDay: Int, endDay: Int, including: repeat DailyWeatherStatisticsQuery<each T>) async throws -> (repeat DailyWeatherStatistics<each T>)](/documentation/weatherkit/weatherservice/dailystatistics(for:startday:endday:including:))
- [func dailySummary<each T>(for: CLLocation, forDaysIn: DateInterval, including: repeat DailyWeatherSummaryQuery<each T>) async throws -> (repeat DailyWeatherSummary<each T>)](/documentation/weatherkit/weatherservice/dailysummary(for:fordaysin:including:))
- [func dailySummary<each T>(for: CLLocation, including: repeat DailyWeatherSummaryQuery<each T>) async throws -> (repeat DailyWeatherSummary<each T>)](/documentation/weatherkit/weatherservice/dailysummary(for:including:))
- [func hourlyStatistics<each T>(for: CLLocation, forHoursIn: DateInterval, including: repeat HourlyWeatherStatisticsQuery<each T>) async throws -> (repeat HourlyWeatherStatistics<each T>)](/documentation/weatherkit/weatherservice/hourlystatistics(for:forhoursin:including:))
- [func hourlyStatistics<each T>(for: CLLocation, including: repeat HourlyWeatherStatisticsQuery<each T>) async throws -> (repeat HourlyWeatherStatistics<each T>)](/documentation/weatherkit/weatherservice/hourlystatistics(for:including:))
- [func hourlyStatistics<each T>(for: CLLocation, startHour: Int, endHour: Int, including: repeat HourlyWeatherStatisticsQuery<each T>) async throws -> (repeat HourlyWeatherStatistics<each T>)](/documentation/weatherkit/weatherservice/hourlystatistics(for:starthour:endhour:including:))
- [func monthlyStatistics<each T>(for: CLLocation, forMonthsIn: DateInterval, including: repeat MonthlyWeatherStatisticsQuery<each T>) async throws -> (repeat MonthlyWeatherStatistics<each T>)](/documentation/weatherkit/weatherservice/monthlystatistics(for:formonthsin:including:))
- [func monthlyStatistics<each T>(for: CLLocation, including: repeat MonthlyWeatherStatisticsQuery<each T>) async throws -> (repeat MonthlyWeatherStatistics<each T>)](/documentation/weatherkit/weatherservice/monthlystatistics(for:including:))
- [func monthlyStatistics<each T>(for: CLLocation, startMonth: Int, endMonth: Int, including: repeat MonthlyWeatherStatisticsQuery<each T>) async throws -> (repeat MonthlyWeatherStatistics<each T>)](/documentation/weatherkit/weatherservice/monthlystatistics(for:startmonth:endmonth:including:))
- [func weather<T>(for: CLLocation, including: WeatherQuery<T>) async throws -> T](/documentation/weatherkit/weatherservice/weather(for:including:)-3cg1d)
- [func weather<each T>(for: CLLocation, including: repeat WeatherQuery<each T>) async throws -> (repeat each T)](/documentation/weatherkit/weatherservice/weather(for:including:)-5jqwy)

## Requests

- [WeatherQuery](/documentation/weatherkit/weatherquery)

### Creating queries

- [static var alerts: WeatherQuery<[WeatherAlert]?>](/documentation/weatherkit/weatherquery/alerts)
- [static var availability: WeatherQuery<WeatherAvailability>](/documentation/weatherkit/weatherquery/availability)
- [static var current: WeatherQuery<CurrentWeather>](/documentation/weatherkit/weatherquery/current)
- [static var daily: WeatherQuery<Forecast<DayWeather>>](/documentation/weatherkit/weatherquery/daily)
- [static var hourly: WeatherQuery<Forecast<HourWeather>>](/documentation/weatherkit/weatherquery/hourly)
- [static var minute: WeatherQuery<Forecast<MinuteWeather>?>](/documentation/weatherkit/weatherquery/minute)
- [static func daily(startDate: Date, endDate: Date) -> WeatherQuery<T>](/documentation/weatherkit/weatherquery/daily(startdate:enddate:))
- [static func hourly(startDate: Date, endDate: Date) -> WeatherQuery<T>](/documentation/weatherkit/weatherquery/hourly(startdate:enddate:))

### Type Properties

- [static var changes: WeatherQuery<WeatherChanges?>](/documentation/weatherkit/weatherquery/changes)
- [static var historicalComparisons: WeatherQuery<HistoricalComparisons?>](/documentation/weatherkit/weatherquery/historicalcomparisons)
- [CurrentWeather](/documentation/weatherkit/currentweather)

### Getting temperature and humidity

- [var apparentTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/currentweather/apparenttemperature)
- [var dewPoint: Measurement<UnitTemperature>](/documentation/weatherkit/currentweather/dewpoint)
- [var humidity: Double](/documentation/weatherkit/currentweather/humidity)
- [var temperature: Measurement<UnitTemperature>](/documentation/weatherkit/currentweather/temperature)

### Getting wind and pressure

- [var pressure: Measurement<UnitPressure>](/documentation/weatherkit/currentweather/pressure)
- [var pressureTrend: PressureTrend](/documentation/weatherkit/currentweather/pressuretrend)
- [var wind: Wind](/documentation/weatherkit/currentweather/wind)

### Getting conditions

- [var cloudCover: Double](/documentation/weatherkit/currentweather/cloudcover)
- [var condition: WeatherCondition](/documentation/weatherkit/currentweather/condition)

### Getting date and validity

- [var date: Date](/documentation/weatherkit/currentweather/date)

### Getting daylight and visibility

- [var isDaylight: Bool](/documentation/weatherkit/currentweather/isdaylight)
- [var uvIndex: UVIndex](/documentation/weatherkit/currentweather/uvindex)
- [var visibility: Measurement<UnitLength>](/documentation/weatherkit/currentweather/visibility)

### Getting additional information

- [var metadata: WeatherMetadata](/documentation/weatherkit/currentweather/metadata)
- [var symbolName: String](/documentation/weatherkit/currentweather/symbolname)

### Instance Properties

- [var cloudCoverByAltitude: CloudCoverByAltitude](/documentation/weatherkit/currentweather/cloudcoverbyaltitude)
- [var precipitationIntensity: Measurement<UnitSpeed>](/documentation/weatherkit/currentweather/precipitationintensity)
- [WeatherAttribution](/documentation/weatherkit/weatherattribution)

### Getting the properties

- [var combinedMarkDarkURL: URL](/documentation/weatherkit/weatherattribution/combinedmarkdarkurl)
- [var combinedMarkLightURL: URL](/documentation/weatherkit/weatherattribution/combinedmarklighturl)
- [var legalPageURL: URL](/documentation/weatherkit/weatherattribution/legalpageurl)
- [var serviceName: String](/documentation/weatherkit/weatherattribution/servicename)
- [var squareMarkURL: URL](/documentation/weatherkit/weatherattribution/squaremarkurl)

### Instance Properties

- [var legalAttributionText: String](/documentation/weatherkit/weatherattribution/legalattributiontext)
- [WeatherMetadata](/documentation/weatherkit/weathermetadata)

### Getting the properties

- [var date: Date](/documentation/weatherkit/weathermetadata/date)
- [var expirationDate: Date](/documentation/weatherkit/weathermetadata/expirationdate)
- [var location: CLLocation](/documentation/weatherkit/weathermetadata/location)
- [WeatherSeverity](/documentation/weatherkit/weatherseverity)

### Getting the properties

- [case minor](/documentation/weatherkit/weatherseverity/minor)
- [case moderate](/documentation/weatherkit/weatherseverity/moderate)
- [case severe](/documentation/weatherkit/weatherseverity/severe)
- [case extreme](/documentation/weatherkit/weatherseverity/extreme)
- [case unknown](/documentation/weatherkit/weatherseverity/unknown)

### Describing the weather severity

- [var accessibilityDescription: String](/documentation/weatherkit/weatherseverity/accessibilitydescription)
- [var description: String](/documentation/weatherkit/weatherseverity/description)

## Characteristics

- [Precipitation](/documentation/weatherkit/precipitation)

### Specifying precipitation types

- [case hail](/documentation/weatherkit/precipitation/hail)
- [case mixed](/documentation/weatherkit/precipitation/mixed)
- [case rain](/documentation/weatherkit/precipitation/rain)
- [case sleet](/documentation/weatherkit/precipitation/sleet)
- [case snow](/documentation/weatherkit/precipitation/snow)
- [case none](/documentation/weatherkit/precipitation/none)

### Describing the precipitation

- [var accessibilityDescription: String](/documentation/weatherkit/precipitation/accessibilitydescription)
- [var description: String](/documentation/weatherkit/precipitation/description)
- [PressureTrend](/documentation/weatherkit/pressuretrend)

### Getting the trend

- [case falling](/documentation/weatherkit/pressuretrend/falling)
- [case rising](/documentation/weatherkit/pressuretrend/rising)
- [case steady](/documentation/weatherkit/pressuretrend/steady)

### Describing the trend

- [var accessibilityDescription: String](/documentation/weatherkit/pressuretrend/accessibilitydescription)
- [var description: String](/documentation/weatherkit/pressuretrend/description)
- [UVIndex](/documentation/weatherkit/uvindex)

### Getting the UV index

- [var category: UVIndex.ExposureCategory](/documentation/weatherkit/uvindex/category)
- [var value: Int](/documentation/weatherkit/uvindex/value)
- [UVIndex.ExposureCategory](/documentation/weatherkit/uvindex/exposurecategory)

#### Enumeration Cases

- [case extreme](/documentation/weatherkit/uvindex/exposurecategory/extreme)
- [case high](/documentation/weatherkit/uvindex/exposurecategory/high)
- [case low](/documentation/weatherkit/uvindex/exposurecategory/low)
- [case moderate](/documentation/weatherkit/uvindex/exposurecategory/moderate)
- [case veryHigh](/documentation/weatherkit/uvindex/exposurecategory/veryhigh)

#### Instance Properties

- [var accessibilityDescription: String](/documentation/weatherkit/uvindex/exposurecategory/accessibilitydescription)
- [var description: String](/documentation/weatherkit/uvindex/exposurecategory/description)
- [var rangeValue: ClosedRange<Int>](/documentation/weatherkit/uvindex/exposurecategory/rangevalue)
- [Wind](/documentation/weatherkit/wind)

### Getting the properties

- [Wind.CompassDirection](/documentation/weatherkit/wind/compassdirection-swift.enum)

#### Describing the compass direction

- [var abbreviation: String](/documentation/weatherkit/wind/compassdirection-swift.enum/abbreviation)
- [var accessibilityDescription: String](/documentation/weatherkit/wind/compassdirection-swift.enum/accessibilitydescription)
- [var description: String](/documentation/weatherkit/wind/compassdirection-swift.enum/description)

#### Enumeration Cases

- [case east](/documentation/weatherkit/wind/compassdirection-swift.enum/east)
- [case eastNortheast](/documentation/weatherkit/wind/compassdirection-swift.enum/eastnortheast)
- [case eastSoutheast](/documentation/weatherkit/wind/compassdirection-swift.enum/eastsoutheast)
- [case north](/documentation/weatherkit/wind/compassdirection-swift.enum/north)
- [case northNortheast](/documentation/weatherkit/wind/compassdirection-swift.enum/northnortheast)
- [case northNorthwest](/documentation/weatherkit/wind/compassdirection-swift.enum/northnorthwest)
- [case northeast](/documentation/weatherkit/wind/compassdirection-swift.enum/northeast)
- [case northwest](/documentation/weatherkit/wind/compassdirection-swift.enum/northwest)
- [case south](/documentation/weatherkit/wind/compassdirection-swift.enum/south)
- [case southSoutheast](/documentation/weatherkit/wind/compassdirection-swift.enum/southsoutheast)
- [case southSouthwest](/documentation/weatherkit/wind/compassdirection-swift.enum/southsouthwest)
- [case southeast](/documentation/weatherkit/wind/compassdirection-swift.enum/southeast)
- [case southwest](/documentation/weatherkit/wind/compassdirection-swift.enum/southwest)
- [case west](/documentation/weatherkit/wind/compassdirection-swift.enum/west)
- [case westNorthwest](/documentation/weatherkit/wind/compassdirection-swift.enum/westnorthwest)
- [case westSouthwest](/documentation/weatherkit/wind/compassdirection-swift.enum/westsouthwest)
- [var compassDirection: Wind.CompassDirection](/documentation/weatherkit/wind/compassdirection-swift.property)
- [var direction: Measurement<UnitAngle>](/documentation/weatherkit/wind/direction)
- [var gust: Measurement<UnitSpeed>?](/documentation/weatherkit/wind/gust)
- [var speed: Measurement<UnitSpeed>](/documentation/weatherkit/wind/speed)
- [WeatherCondition](/documentation/weatherkit/weathercondition)

### Getting visibility properties

- [case blowingDust](/documentation/weatherkit/weathercondition/blowingdust)
- [case clear](/documentation/weatherkit/weathercondition/clear)
- [case cloudy](/documentation/weatherkit/weathercondition/cloudy)
- [case foggy](/documentation/weatherkit/weathercondition/foggy)
- [case haze](/documentation/weatherkit/weathercondition/haze)
- [case mostlyClear](/documentation/weatherkit/weathercondition/mostlyclear)
- [case mostlyCloudy](/documentation/weatherkit/weathercondition/mostlycloudy)
- [case partlyCloudy](/documentation/weatherkit/weathercondition/partlycloudy)
- [case smoky](/documentation/weatherkit/weathercondition/smoky)

### Getting wind properties

- [case breezy](/documentation/weatherkit/weathercondition/breezy)
- [case windy](/documentation/weatherkit/weathercondition/windy)

### Getting precipitation properties

- [case drizzle](/documentation/weatherkit/weathercondition/drizzle)
- [case heavyRain](/documentation/weatherkit/weathercondition/heavyrain)
- [case isolatedThunderstorms](/documentation/weatherkit/weathercondition/isolatedthunderstorms)
- [case rain](/documentation/weatherkit/weathercondition/rain)
- [case sunShowers](/documentation/weatherkit/weathercondition/sunshowers)
- [case scatteredThunderstorms](/documentation/weatherkit/weathercondition/scatteredthunderstorms)
- [case strongStorms](/documentation/weatherkit/weathercondition/strongstorms)
- [case thunderstorms](/documentation/weatherkit/weathercondition/thunderstorms)

### Getting hazardous properties

- [case frigid](/documentation/weatherkit/weathercondition/frigid)
- [case hail](/documentation/weatherkit/weathercondition/hail)
- [case hot](/documentation/weatherkit/weathercondition/hot)

### Getting winter precipitation properties

- [case flurries](/documentation/weatherkit/weathercondition/flurries)
- [case sleet](/documentation/weatherkit/weathercondition/sleet)
- [case snow](/documentation/weatherkit/weathercondition/snow)
- [case sunFlurries](/documentation/weatherkit/weathercondition/sunflurries)
- [case wintryMix](/documentation/weatherkit/weathercondition/wintrymix)

### Getting hazardous winter properties

- [case blizzard](/documentation/weatherkit/weathercondition/blizzard)
- [case blowingSnow](/documentation/weatherkit/weathercondition/blowingsnow)
- [case freezingDrizzle](/documentation/weatherkit/weathercondition/freezingdrizzle)
- [case freezingRain](/documentation/weatherkit/weathercondition/freezingrain)
- [case heavySnow](/documentation/weatherkit/weathercondition/heavysnow)

### Getting tropical hazard properties

- [case hurricane](/documentation/weatherkit/weathercondition/hurricane)
- [case tropicalStorm](/documentation/weatherkit/weathercondition/tropicalstorm)

### Describing the weather condition

- [var accessibilityDescription: String](/documentation/weatherkit/weathercondition/accessibilitydescription)
- [var description: String](/documentation/weatherkit/weathercondition/description)

## Alerts and forecasts

- [WeatherAlert](/documentation/weatherkit/weatheralert)

### Getting the properties

- [var metadata: WeatherMetadata](/documentation/weatherkit/weatheralert/metadata)
- [var region: String?](/documentation/weatherkit/weatheralert/region)
- [var severity: WeatherSeverity](/documentation/weatherkit/weatheralert/severity)
- [var summary: String](/documentation/weatherkit/weatheralert/summary)

### Providing attribution

- [var detailsURL: URL](/documentation/weatherkit/weatheralert/detailsurl)
- [var source: String](/documentation/weatherkit/weatheralert/source)
- [WeatherAvailability](/documentation/weatherkit/weatheravailability)

### Getting the properties

- [var alertAvailability: WeatherAvailability.AvailabilityKind](/documentation/weatherkit/weatheravailability/alertavailability)
- [var minuteAvailability: WeatherAvailability.AvailabilityKind](/documentation/weatherkit/weatheravailability/minuteavailability)
- [WeatherAvailability.AvailabilityKind](/documentation/weatherkit/weatheravailability/availabilitykind)

#### Enumeration Cases

- [case available](/documentation/weatherkit/weatheravailability/availabilitykind/available)
- [case temporarilyUnavailable](/documentation/weatherkit/weatheravailability/availabilitykind/temporarilyunavailable)
- [case unknown](/documentation/weatherkit/weatheravailability/availabilitykind/unknown)
- [case unsupported](/documentation/weatherkit/weatheravailability/availabilitykind/unsupported)
- [Forecast](/documentation/weatherkit/forecast)

### Creating the forecast

- [init(from: any Decoder) throws](/documentation/weatherkit/forecast/init(from:)-390k1)
- [init(from: any Decoder) throws](/documentation/weatherkit/forecast/init(from:)-4wobg)

### Serializing objects

- [func encode(to: any Encoder) throws](/documentation/weatherkit/forecast/encode(to:)-5zuqd)
- [func encode(to: any Encoder) throws](/documentation/weatherkit/forecast/encode(to:)-fbco)

### Getting the properties

- [var endIndex: Forecast<Element>.Index](/documentation/weatherkit/forecast/endindex)
- [var forecast: [Element]](/documentation/weatherkit/forecast/forecast)
- [var metadata: WeatherMetadata](/documentation/weatherkit/forecast/metadata)
- [var startIndex: Forecast<Element>.Index](/documentation/weatherkit/forecast/startindex)
- [var summary: String](/documentation/weatherkit/forecast/summary)

### Accessing elements

- [subscript(Forecast<Element>.Index) -> Element](/documentation/weatherkit/forecast/subscript(_:))
- [Forecast.Index](/documentation/weatherkit/forecast/index)

### Comparing forecasts

- [static func == (Forecast<MinuteWeather>, Forecast<MinuteWeather>) -> Bool](/documentation/weatherkit/forecast/==(_:_:))
- [MinuteWeather](/documentation/weatherkit/minuteweather)

### Getting the precipitation

- [var precipitation: Precipitation](/documentation/weatherkit/minuteweather/precipitation)
- [var precipitationChance: Double](/documentation/weatherkit/minuteweather/precipitationchance)
- [var precipitationIntensity: Measurement<UnitSpeed>](/documentation/weatherkit/minuteweather/precipitationintensity)

### Getting the date

- [var date: Date](/documentation/weatherkit/minuteweather/date)
- [HourWeather](/documentation/weatherkit/hourweather)

### Getting temperature and humidity

- [var apparentTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/hourweather/apparenttemperature)
- [var humidity: Double](/documentation/weatherkit/hourweather/humidity)
- [var temperature: Measurement<UnitTemperature>](/documentation/weatherkit/hourweather/temperature)
- [var dewPoint: Measurement<UnitTemperature>](/documentation/weatherkit/hourweather/dewpoint)

### Getting pressure

- [var pressure: Measurement<UnitPressure>](/documentation/weatherkit/hourweather/pressure)
- [var pressureTrend: PressureTrend](/documentation/weatherkit/hourweather/pressuretrend)

### Getting conditions

- [var cloudCover: Double](/documentation/weatherkit/hourweather/cloudcover)
- [var condition: WeatherCondition](/documentation/weatherkit/hourweather/condition)
- [var isDaylight: Bool](/documentation/weatherkit/hourweather/isdaylight)
- [var visibility: Measurement<UnitLength>](/documentation/weatherkit/hourweather/visibility)

### Getting the UV index

- [var uvIndex: UVIndex](/documentation/weatherkit/hourweather/uvindex)

### Getting the wind

- [var wind: Wind](/documentation/weatherkit/hourweather/wind)

### Getting the date

- [var date: Date](/documentation/weatherkit/hourweather/date)

### Getting the precipitation

- [var precipitation: Precipitation](/documentation/weatherkit/hourweather/precipitation)
- [var precipitationChance: Double](/documentation/weatherkit/hourweather/precipitationchance)

### Getting the weather symbol

- [var symbolName: String](/documentation/weatherkit/hourweather/symbolname)

### Instance Properties

- [var cloudCoverByAltitude: CloudCoverByAltitude](/documentation/weatherkit/hourweather/cloudcoverbyaltitude)
- [var precipitationAmount: Measurement<UnitLength>](/documentation/weatherkit/hourweather/precipitationamount)
- [var snowfallAmount: Measurement<UnitLength>](/documentation/weatherkit/hourweather/snowfallamount)
- [DayWeather](/documentation/weatherkit/dayweather)

### Getting temperature

- [var highTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/dayweather/hightemperature)
- [var lowTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/dayweather/lowtemperature)

### Getting precipitation

- [var precipitation: Precipitation](/documentation/weatherkit/dayweather/precipitation)
- [var precipitationChance: Double](/documentation/weatherkit/dayweather/precipitationchance)
- [var rainfallAmount: Measurement<UnitLength>](/documentation/weatherkit/dayweather/rainfallamount)
- [var snowfallAmount: Measurement<UnitLength>](/documentation/weatherkit/dayweather/snowfallamount)

### Getting celestial information

- [var moon: MoonEvents](/documentation/weatherkit/dayweather/moon)
- [var sun: SunEvents](/documentation/weatherkit/dayweather/sun)

### Getting the wind

- [var wind: Wind](/documentation/weatherkit/dayweather/wind)

### Getting the date

- [var date: Date](/documentation/weatherkit/dayweather/date)

### Getting condition and UV index

- [var condition: WeatherCondition](/documentation/weatherkit/dayweather/condition)
- [var uvIndex: UVIndex](/documentation/weatherkit/dayweather/uvindex)

### Getting the weather symbol

- [var symbolName: String](/documentation/weatherkit/dayweather/symbolname)

### Instance Properties

- [var daytimeForecast: DayPartForecast](/documentation/weatherkit/dayweather/daytimeforecast)
- [var highTemperatureTime: Date?](/documentation/weatherkit/dayweather/hightemperaturetime)
- [var highWindSpeed: Measurement<UnitSpeed>?](/documentation/weatherkit/dayweather/highwindspeed)
- [var lowTemperatureTime: Date?](/documentation/weatherkit/dayweather/lowtemperaturetime)
- [var maximumHumidity: Double](/documentation/weatherkit/dayweather/maximumhumidity)
- [var maximumVisibility: Double](/documentation/weatherkit/dayweather/maximumvisibility)
- [var minimumHumidity: Double](/documentation/weatherkit/dayweather/minimumhumidity)
- [var minimumVisibility: Double](/documentation/weatherkit/dayweather/minimumvisibility)
- [var overnightForecast: DayPartForecast](/documentation/weatherkit/dayweather/overnightforecast)
- [var precipitationAmount: Measurement<UnitLength>](/documentation/weatherkit/dayweather/precipitationamount)
- [var precipitationAmountByType: PrecipitationAmountByType](/documentation/weatherkit/dayweather/precipitationamountbytype)
- [var restOfDayForecast: DayPartForecast?](/documentation/weatherkit/dayweather/restofdayforecast)

## Celestial information

- [SunEvents](/documentation/weatherkit/sunevents)

### Getting the sun events

- [var astronomicalDawn: Date?](/documentation/weatherkit/sunevents/astronomicaldawn)
- [var astronomicalDusk: Date?](/documentation/weatherkit/sunevents/astronomicaldusk)
- [var civilDawn: Date?](/documentation/weatherkit/sunevents/civildawn)
- [var civilDusk: Date?](/documentation/weatherkit/sunevents/civildusk)
- [var nauticalDawn: Date?](/documentation/weatherkit/sunevents/nauticaldawn)
- [var nauticalDusk: Date?](/documentation/weatherkit/sunevents/nauticaldusk)
- [var solarMidnight: Date?](/documentation/weatherkit/sunevents/solarmidnight)
- [var solarNoon: Date?](/documentation/weatherkit/sunevents/solarnoon)
- [var sunrise: Date?](/documentation/weatherkit/sunevents/sunrise)
- [var sunset: Date?](/documentation/weatherkit/sunevents/sunset)
- [MoonEvents](/documentation/weatherkit/moonevents)

### Getting the moon events

- [var moonrise: Date?](/documentation/weatherkit/moonevents/moonrise)
- [var moonset: Date?](/documentation/weatherkit/moonevents/moonset)
- [var phase: MoonPhase](/documentation/weatherkit/moonevents/phase)
- [MoonPhase](/documentation/weatherkit/moonphase)

### Getting the moon phase

- [case firstQuarter](/documentation/weatherkit/moonphase/firstquarter)
- [case full](/documentation/weatherkit/moonphase/full)
- [case lastQuarter](/documentation/weatherkit/moonphase/lastquarter)
- [case new](/documentation/weatherkit/moonphase/new)
- [case waningCrescent](/documentation/weatherkit/moonphase/waningcrescent)
- [case waningGibbous](/documentation/weatherkit/moonphase/waninggibbous)
- [case waxingCrescent](/documentation/weatherkit/moonphase/waxingcrescent)
- [case waxingGibbous](/documentation/weatherkit/moonphase/waxinggibbous)

### Describing the moon phase

- [var accessibilityDescription: String](/documentation/weatherkit/moonphase/accessibilitydescription)
- [var description: String](/documentation/weatherkit/moonphase/description)
- [var symbolName: String](/documentation/weatherkit/moonphase/symbolname)

## Errors

- [WeatherError](/documentation/weatherkit/weathererror)

### Getting the error type

- [case permissionDenied](/documentation/weatherkit/weathererror/permissiondenied)
- [case unknown](/documentation/weatherkit/weathererror/unknown)

### Getting the error properties

- [var errorDescription: String?](/documentation/weatherkit/weathererror/errordescription)
- [var failureReason: String?](/documentation/weatherkit/weathererror/failurereason)
- [var helpAnchor: String?](/documentation/weatherkit/weathererror/helpanchor)
- [var recoverySuggestion: String?](/documentation/weatherkit/weathererror/recoverysuggestion)

## Structures

- [CloudCoverByAltitude](/documentation/weatherkit/cloudcoverbyaltitude)

### Instance Properties

- [var high: Double](/documentation/weatherkit/cloudcoverbyaltitude/high)
- [var low: Double](/documentation/weatherkit/cloudcoverbyaltitude/low)
- [var medium: Double](/documentation/weatherkit/cloudcoverbyaltitude/medium)
- [DailyWeatherStatistics](/documentation/weatherkit/dailyweatherstatistics)

### Instance Properties

- [var baselineStartDate: Date](/documentation/weatherkit/dailyweatherstatistics/baselinestartdate)
- [var days: [T]](/documentation/weatherkit/dailyweatherstatistics/days)
- [var endIndex: DailyWeatherStatistics<T>.Index](/documentation/weatherkit/dailyweatherstatistics/endindex)
- [var metadata: WeatherMetadata](/documentation/weatherkit/dailyweatherstatistics/metadata)
- [var startIndex: DailyWeatherStatistics<T>.Index](/documentation/weatherkit/dailyweatherstatistics/startindex)

### Subscripts

- [subscript(DailyWeatherStatistics<T>.Index) -> DailyWeatherStatistics<T>.Element](/documentation/weatherkit/dailyweatherstatistics/subscript(_:))
- [DailyWeatherStatisticsQuery](/documentation/weatherkit/dailyweatherstatisticsquery)

### Type Properties

- [static var precipitation: DailyWeatherStatisticsQuery<DayPrecipitationStatistics>](/documentation/weatherkit/dailyweatherstatisticsquery/precipitation)
- [static var temperature: DailyWeatherStatisticsQuery<DayTemperatureStatistics>](/documentation/weatherkit/dailyweatherstatisticsquery/temperature)
- [DailyWeatherSummary](/documentation/weatherkit/dailyweathersummary)

### Instance Properties

- [var days: [T]](/documentation/weatherkit/dailyweathersummary/days)
- [var endIndex: DailyWeatherSummary<T>.Index](/documentation/weatherkit/dailyweathersummary/endindex)
- [var metadata: WeatherMetadata](/documentation/weatherkit/dailyweathersummary/metadata)
- [var startIndex: DailyWeatherSummary<T>.Index](/documentation/weatherkit/dailyweathersummary/startindex)

### Subscripts

- [subscript(DailyWeatherSummary<T>.Index) -> DailyWeatherSummary<T>.Element](/documentation/weatherkit/dailyweathersummary/subscript(_:))
- [DailyWeatherSummaryQuery](/documentation/weatherkit/dailyweathersummaryquery)

### Type Properties

- [static var precipitation: DailyWeatherSummaryQuery<DayPrecipitationSummary>](/documentation/weatherkit/dailyweathersummaryquery/precipitation)
- [static var temperature: DailyWeatherSummaryQuery<DayTemperatureSummary>](/documentation/weatherkit/dailyweathersummaryquery/temperature)
- [DayPartForecast](/documentation/weatherkit/daypartforecast)

### Instance Properties

- [var cloudCover: Double](/documentation/weatherkit/daypartforecast/cloudcover)
- [var cloudCoverByAltitude: CloudCoverByAltitude](/documentation/weatherkit/daypartforecast/cloudcoverbyaltitude)
- [var condition: WeatherCondition](/documentation/weatherkit/daypartforecast/condition)
- [var highTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/daypartforecast/hightemperature)
- [var highWindSpeed: Measurement<UnitSpeed>](/documentation/weatherkit/daypartforecast/highwindspeed)
- [var lowTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/daypartforecast/lowtemperature)
- [var maximumHumidity: Double](/documentation/weatherkit/daypartforecast/maximumhumidity)
- [var maximumVisibility: Measurement<UnitLength>](/documentation/weatherkit/daypartforecast/maximumvisibility)
- [var minimumHumidity: Double](/documentation/weatherkit/daypartforecast/minimumhumidity)
- [var minimumVisibility: Measurement<UnitLength>](/documentation/weatherkit/daypartforecast/minimumvisibility)
- [var precipitation: Precipitation](/documentation/weatherkit/daypartforecast/precipitation)
- [var precipitationAmountByType: PrecipitationAmountByType](/documentation/weatherkit/daypartforecast/precipitationamountbytype)
- [var precipitationChance: Double](/documentation/weatherkit/daypartforecast/precipitationchance)
- [var wind: Wind](/documentation/weatherkit/daypartforecast/wind)
- [DayPrecipitationStatistics](/documentation/weatherkit/dayprecipitationstatistics)

### Instance Properties

- [var averagePrecipitationAmount: Measurement<UnitLength>](/documentation/weatherkit/dayprecipitationstatistics/averageprecipitationamount)
- [var averagePrecipitationProbability: Double](/documentation/weatherkit/dayprecipitationstatistics/averageprecipitationprobability)
- [var averageSnowfallAmount: Measurement<UnitLength>](/documentation/weatherkit/dayprecipitationstatistics/averagesnowfallamount)
- [var day: Int](/documentation/weatherkit/dayprecipitationstatistics/day)
- [DayPrecipitationSummary](/documentation/weatherkit/dayprecipitationsummary)

### Instance Properties

- [var date: Date](/documentation/weatherkit/dayprecipitationsummary/date)
- [var precipitationAmount: Measurement<UnitLength>](/documentation/weatherkit/dayprecipitationsummary/precipitationamount)
- [var snowfallAmount: Measurement<UnitLength>](/documentation/weatherkit/dayprecipitationsummary/snowfallamount)
- [DayTemperatureStatistics](/documentation/weatherkit/daytemperaturestatistics)

### Instance Properties

- [var averageHighTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/daytemperaturestatistics/averagehightemperature)
- [var averageLowTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/daytemperaturestatistics/averagelowtemperature)
- [var day: Int](/documentation/weatherkit/daytemperaturestatistics/day)
- [DayTemperatureSummary](/documentation/weatherkit/daytemperaturesummary)

### Instance Properties

- [var date: Date](/documentation/weatherkit/daytemperaturesummary/date)
- [var highTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/daytemperaturesummary/hightemperature)
- [var lowTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/daytemperaturesummary/lowtemperature)
- [HistoricalComparisons](/documentation/weatherkit/historicalcomparisons)

### Instance Properties

- [var comparisons: [HistoricalComparison]](/documentation/weatherkit/historicalcomparisons/comparisons)
- [var endIndex: HistoricalComparisons.Index](/documentation/weatherkit/historicalcomparisons/endindex)
- [var metadata: WeatherMetadata](/documentation/weatherkit/historicalcomparisons/metadata)
- [var startIndex: HistoricalComparisons.Index](/documentation/weatherkit/historicalcomparisons/startindex)

### Subscripts

- [subscript(HistoricalComparisons.Index) -> HistoricalComparisons.Element](/documentation/weatherkit/historicalcomparisons/subscript(_:))
- [HourTemperatureStatistics](/documentation/weatherkit/hourtemperaturestatistics)

### Instance Properties

- [var hour: Int](/documentation/weatherkit/hourtemperaturestatistics/hour)
- [var percentiles: Percentiles<UnitTemperature>](/documentation/weatherkit/hourtemperaturestatistics/percentiles)
- [HourlyWeatherStatistics](/documentation/weatherkit/hourlyweatherstatistics)

### Instance Properties

- [var baselineStartDate: Date](/documentation/weatherkit/hourlyweatherstatistics/baselinestartdate)
- [var endIndex: HourlyWeatherStatistics<T>.Index](/documentation/weatherkit/hourlyweatherstatistics/endindex)
- [var hours: [T]](/documentation/weatherkit/hourlyweatherstatistics/hours)
- [var metadata: WeatherMetadata](/documentation/weatherkit/hourlyweatherstatistics/metadata)
- [var startIndex: HourlyWeatherStatistics<T>.Index](/documentation/weatherkit/hourlyweatherstatistics/startindex)

### Subscripts

- [subscript(HourlyWeatherStatistics<T>.Index) -> HourlyWeatherStatistics<T>.Element](/documentation/weatherkit/hourlyweatherstatistics/subscript(_:))
- [HourlyWeatherStatisticsQuery](/documentation/weatherkit/hourlyweatherstatisticsquery)

### Type Properties

- [static var temperature: HourlyWeatherStatisticsQuery<HourTemperatureStatistics>](/documentation/weatherkit/hourlyweatherstatisticsquery/temperature)
- [MonthPrecipitationStatistics](/documentation/weatherkit/monthprecipitationstatistics)

### Instance Properties

- [var averagePrecipitationAmount: Measurement<UnitLength>](/documentation/weatherkit/monthprecipitationstatistics/averageprecipitationamount)
- [var averagePrecipitationProbability: Double](/documentation/weatherkit/monthprecipitationstatistics/averageprecipitationprobability)
- [var averageSnowfallAmount: Measurement<UnitLength>](/documentation/weatherkit/monthprecipitationstatistics/averagesnowfallamount)
- [var month: Int](/documentation/weatherkit/monthprecipitationstatistics/month)
- [MonthTemperatureStatistics](/documentation/weatherkit/monthtemperaturestatistics)

### Instance Properties

- [var averageHighTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/monthtemperaturestatistics/averagehightemperature)
- [var averageLowTemperature: Measurement<UnitTemperature>](/documentation/weatherkit/monthtemperaturestatistics/averagelowtemperature)
- [var month: Int](/documentation/weatherkit/monthtemperaturestatistics/month)
- [MonthlyWeatherStatistics](/documentation/weatherkit/monthlyweatherstatistics)

### Instance Properties

- [var baselineStartDate: Date](/documentation/weatherkit/monthlyweatherstatistics/baselinestartdate)
- [var endIndex: MonthlyWeatherStatistics<T>.Index](/documentation/weatherkit/monthlyweatherstatistics/endindex)
- [var metadata: WeatherMetadata](/documentation/weatherkit/monthlyweatherstatistics/metadata)
- [var months: [T]](/documentation/weatherkit/monthlyweatherstatistics/months)
- [var startIndex: MonthlyWeatherStatistics<T>.Index](/documentation/weatherkit/monthlyweatherstatistics/startindex)

### Subscripts

- [subscript(MonthlyWeatherStatistics<T>.Index) -> MonthlyWeatherStatistics<T>.Element](/documentation/weatherkit/monthlyweatherstatistics/subscript(_:))
- [MonthlyWeatherStatisticsQuery](/documentation/weatherkit/monthlyweatherstatisticsquery)

### Type Properties

- [static var precipitation: MonthlyWeatherStatisticsQuery<MonthPrecipitationStatistics>](/documentation/weatherkit/monthlyweatherstatisticsquery/precipitation)
- [static var temperature: MonthlyWeatherStatisticsQuery<MonthTemperatureStatistics>](/documentation/weatherkit/monthlyweatherstatisticsquery/temperature)
- [Percentiles](/documentation/weatherkit/percentiles)

### Instance Properties

- [var p10: Measurement<Dimension>](/documentation/weatherkit/percentiles/p10)
- [var p50: Measurement<Dimension>](/documentation/weatherkit/percentiles/p50)
- [var p90: Measurement<Dimension>](/documentation/weatherkit/percentiles/p90)
- [PrecipitationAmountByType](/documentation/weatherkit/precipitationamountbytype)

### Instance Properties

- [var hail: Measurement<UnitLength>](/documentation/weatherkit/precipitationamountbytype/hail)
- [var mixed: Measurement<UnitLength>](/documentation/weatherkit/precipitationamountbytype/mixed)
- [var precipitation: Measurement<UnitLength>](/documentation/weatherkit/precipitationamountbytype/precipitation)
- [var rainfall: Measurement<UnitLength>](/documentation/weatherkit/precipitationamountbytype/rainfall)
- [var sleet: Measurement<UnitLength>](/documentation/weatherkit/precipitationamountbytype/sleet)
- [var snowfallAmount: SnowfallAmount](/documentation/weatherkit/precipitationamountbytype/snowfallamount)
- [SnowfallAmount](/documentation/weatherkit/snowfallamount)

### Instance Properties

- [var amount: Measurement<UnitLength>](/documentation/weatherkit/snowfallamount/amount)
- [var amountLiquidEquivalent: Measurement<UnitLength>](/documentation/weatherkit/snowfallamount/amountliquidequivalent)
- [var maximum: Measurement<UnitLength>](/documentation/weatherkit/snowfallamount/maximum)
- [var maximumLiquidEquivalent: Measurement<UnitLength>](/documentation/weatherkit/snowfallamount/maximumliquidequivalent)
- [var minimum: Measurement<UnitLength>](/documentation/weatherkit/snowfallamount/minimum)
- [var minimumLiquidEquivalent: Measurement<UnitLength>](/documentation/weatherkit/snowfallamount/minimumliquidequivalent)
- [Trend](/documentation/weatherkit/trend)

### Instance Properties

- [var baseline: TrendBaseline<Dimension>](/documentation/weatherkit/trend/baseline)
- [var currentValue: Measurement<Dimension>](/documentation/weatherkit/trend/currentvalue)
- [var deviation: Deviation](/documentation/weatherkit/trend/deviation)
- [TrendBaseline](/documentation/weatherkit/trendbaseline)

### Instance Properties

- [let kind: TrendBaseline<Dimension>.Kind](/documentation/weatherkit/trendbaseline/kind-swift.property)
- [let startDate: Date](/documentation/weatherkit/trendbaseline/startdate)
- [let value: Measurement<Dimension>](/documentation/weatherkit/trendbaseline/value)

### Enumerations

- [TrendBaseline.Kind](/documentation/weatherkit/trendbaseline/kind-swift.enum)

#### Enumeration Cases

- [case mean](/documentation/weatherkit/trendbaseline/kind-swift.enum/mean)
- [WeatherChange](/documentation/weatherkit/weatherchange)

### Instance Properties

- [var date: Date](/documentation/weatherkit/weatherchange/date)
- [var dayPrecipitationAmount: WeatherChange.Direction](/documentation/weatherkit/weatherchange/dayprecipitationamount)
- [var highTemperature: WeatherChange.Direction](/documentation/weatherkit/weatherchange/hightemperature)
- [var lowTemperature: WeatherChange.Direction](/documentation/weatherkit/weatherchange/lowtemperature)
- [var nightPrecipitationAmount: WeatherChange.Direction](/documentation/weatherkit/weatherchange/nightprecipitationamount)

### Enumerations

- [WeatherChange.Direction](/documentation/weatherkit/weatherchange/direction)

#### Enumeration Cases

- [case decrease](/documentation/weatherkit/weatherchange/direction/decrease)
- [case increase](/documentation/weatherkit/weatherchange/direction/increase)
- [case steady](/documentation/weatherkit/weatherchange/direction/steady)
- [WeatherChanges](/documentation/weatherkit/weatherchanges)

### Instance Properties

- [var changes: [WeatherChange]](/documentation/weatherkit/weatherchanges/changes)
- [var endIndex: WeatherChanges.Index](/documentation/weatherkit/weatherchanges/endindex)
- [var metadata: WeatherMetadata](/documentation/weatherkit/weatherchanges/metadata)
- [var startIndex: WeatherChanges.Index](/documentation/weatherkit/weatherchanges/startindex)

### Subscripts

- [subscript(WeatherChanges.Index) -> WeatherChanges.Element](/documentation/weatherkit/weatherchanges/subscript(_:))

## Enumerations

- [Deviation](/documentation/weatherkit/deviation)

### Enumeration Cases

- [case higher](/documentation/weatherkit/deviation/higher)
- [case lower](/documentation/weatherkit/deviation/lower)
- [case muchHigher](/documentation/weatherkit/deviation/muchhigher)
- [case muchLower](/documentation/weatherkit/deviation/muchlower)
- [case normal](/documentation/weatherkit/deviation/normal)
- [HistoricalComparison](/documentation/weatherkit/historicalcomparison)

### Enumeration Cases

- [case highTemperature(Trend<UnitTemperature>)](/documentation/weatherkit/historicalcomparison/hightemperature(_:))
- [case lowTemperature(Trend<UnitTemperature>)](/documentation/weatherkit/historicalcomparison/lowtemperature(_:))
- [case precipitationAmount(Trend<UnitLength>)](/documentation/weatherkit/historicalcomparison/precipitationamount(_:))
- [case snowfallAmount(Trend<UnitLength>)](/documentation/weatherkit/historicalcomparison/snowfallamount(_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
