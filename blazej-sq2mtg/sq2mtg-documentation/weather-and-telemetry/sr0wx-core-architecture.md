# SR0WX — Core Architecture

## Purpose

SR0WX is an automatic amateur-radio weather-station application. It collects weather and environmental data, converts the information into audio samples and plays the resulting announcement through a radio connected to the station computer.

The SQ2MTG fork is used by the UMG Scientific Club “SZKUNER” SP2ZIE for station SR2WXG. The README documents **144.950 MHz** as the station frequency.

## Processing model

The repository README describes a modular, concurrent architecture:

1. individual data modules acquire information from external or local sources;
2. modules convert their results into announcement words/samples;
3. modules can execute concurrently using multiprocessing;
4. the main application assembles the announcement and controls playback;
5. fallback modules can be used when a primary module fails.

A test mode allows module execution without transmitting/playing the generated samples.

## Documented modules

The fork includes modules for sunrise/sunset calculation, PAA radiation data, Baltic forecast, IMGW warnings, UDP weather-station data, space-weather alerts, radio propagation/noise, experimental yr.no weather, forest-fire danger, weather radar, Polish power-grid state and IMGW water-level data.

## Runtime evolution

The README records migration from Python 2 to Python 3, replacement of urllib with requests in relevant modules, retry behavior for failed downloads, coloredlogs logging, a cache directory and relocation of modules into modules/.

Station-specific parameters, including API keys, are intended to be kept in .env rather than embedded in source.

## Configuration and verification boundaries

The README does not fully define the process supervisor, audio device parameters, exact environment-variable names, module interfaces or external response schemas. Those details should be verified directly against source code and the project wiki before being treated as stable interfaces.

## Planned integration

The README lists APRS-based weather-station data acquisition as planned work.

## Security

The station combines Internet data acquisition with a radio transmission path. Run the application with the minimum required privileges, restrict outbound/inbound access where practical and keep API credentials outside source control.

## Source

Repository: SQ2MTG/sr0wx
