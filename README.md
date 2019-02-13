![App Brewery Banner](Documentation/AppBreweryBanner.png)

# Clima

## My Goal

In this spike project I'll be exploring interaction of an iOS app with external APIs and also the use of open-source libraries (CocoaPods).

## What I will create

We're going to create a simple weather app.

## Specific aims

* How to use CocoaPods to manage and use open source code libraries.
* How to use the Command Line on Mac with Terminal.
* Learn about Networking calls.
* Use public web-based APIs to fetch data.
* How to parse data organised in JSON format.
* Learn about Core Location and utilising the iPhone’s inbuilt GPS.
* Learn about navigation between View Controllers using Segues.
* Introduction to Delegates and Protocols.
* How to pass data between View Controllers.
* Learn and use Switch statements

The following are some notes/fixes I may need during certain parts of the app construction.

## Fix for Cocoapods v1.0.1 and below

```ruby
post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '3.0'
      config.build_settings['MACOSX_DEPLOYMENT_TARGET'] = '10.10'
    end
  end
end
```

## Fix for App Transport Security Override

```XML
	<key>NSAppTransportSecurity</key>
	<dict>
		<key>NSExceptionDomains</key>
		<dict>
			<key>openweathermap.org</key>
			<dict>
				<key>NSIncludesSubdomains</key>
				<true/>
				<key>NSTemporaryExceptionAllowsInsecureHTTPLoads</key>
				<true/>
			</dict>
		</dict>
	</dict>
```

>This is a companion project to The App Brewery's Complete App Developement Bootcamp, check out the full course at [www.appbrewery.co](https://www.appbrewery.co/)

![End Banner](Documentation/readme-end-banner.png)
