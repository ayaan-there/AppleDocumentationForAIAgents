# GeoToolbox Documentation

Source: https://sosumi.ai/documentation/geotoolbox

---
title: GeoToolbox
source: https://developer.apple.com/documentation/geotoolbox
timestamp: 2026-02-13T18:57:38.333Z
---

## Getting rich information about a place

- [PlaceDescriptor](/documentation/geotoolbox/placedescriptor)

### Creating place descriptors

- [init(representations: [PlaceDescriptor.PlaceRepresentation], commonName: String?, supportingRepresentations: [PlaceDescriptor.SupportingPlaceRepresentation])](/documentation/geotoolbox/placedescriptor/init(representations:commonname:supportingrepresentations:))
- [init?(item: MKMapItem)](/documentation/geotoolbox/placedescriptor/init(item:))

### Getting the attributes of a place descriptor

- [let commonName: String?](/documentation/geotoolbox/placedescriptor/commonname)
- [var address: String?](/documentation/geotoolbox/placedescriptor/address)
- [var coordinate: CLLocationCoordinate2D?](/documentation/geotoolbox/placedescriptor/coordinate)
- [let representations: [PlaceDescriptor.PlaceRepresentation]](/documentation/geotoolbox/placedescriptor/representations)
- [let supportingRepresentations: [PlaceDescriptor.SupportingPlaceRepresentation]](/documentation/geotoolbox/placedescriptor/supportingrepresentations)
- [func serviceIdentifier(for: String) -> String?](/documentation/geotoolbox/placedescriptor/serviceidentifier(for:))

### Enumeration values that describe places and mapping service representations

- [PlaceDescriptor.PlaceRepresentation](/documentation/geotoolbox/placedescriptor/placerepresentation)

#### Place representations

- [var address: String?](/documentation/geotoolbox/placedescriptor/address)
- [var coordinate: CLLocationCoordinate2D?](/documentation/geotoolbox/placedescriptor/coordinate)

#### Enumeration cases

- [case address(String)](/documentation/geotoolbox/placedescriptor/placerepresentation/address(_:))
- [case coordinate(CLLocationCoordinate2D)](/documentation/geotoolbox/placedescriptor/placerepresentation/coordinate(_:))
- [case deviceLocation(CLLocation)](/documentation/geotoolbox/placedescriptor/placerepresentation/devicelocation(_:))
- [PlaceDescriptor.SupportingPlaceRepresentation](/documentation/geotoolbox/placedescriptor/supportingplacerepresentation)

#### Getting available supporting representations

- [case serviceIdentifiers([String : String])](/documentation/geotoolbox/placedescriptor/supportingplacerepresentation/serviceidentifiers(_:))

### Type Aliases

- [PlaceDescriptor.Specification](/documentation/geotoolbox/placedescriptor/specification)
- [PlaceDescriptor.UnwrappedType](/documentation/geotoolbox/placedescriptor/unwrappedtype)
- [PlaceDescriptor.ValueType](/documentation/geotoolbox/placedescriptor/valuetype)

### Type Properties

- [static var defaultResolverSpecification: some ResolverSpecification](/documentation/geotoolbox/placedescriptor/defaultresolverspecification)

## Creating a place descriptor

- [init?(item: MKMapItem)](/documentation/geotoolbox/placedescriptor/init(item:))
- [init(representations: [PlaceDescriptor.PlaceRepresentation], commonName: String?, supportingRepresentations: [PlaceDescriptor.SupportingPlaceRepresentation])](/documentation/geotoolbox/placedescriptor/init(representations:commonname:supportingrepresentations:))

## Values that describe places and mapping service providers

- [PlaceDescriptor.PlaceRepresentation](/documentation/geotoolbox/placedescriptor/placerepresentation)

### Place representations

- [var address: String?](/documentation/geotoolbox/placedescriptor/address)
- [var coordinate: CLLocationCoordinate2D?](/documentation/geotoolbox/placedescriptor/coordinate)

### Enumeration cases

- [case address(String)](/documentation/geotoolbox/placedescriptor/placerepresentation/address(_:))
- [case coordinate(CLLocationCoordinate2D)](/documentation/geotoolbox/placedescriptor/placerepresentation/coordinate(_:))
- [case deviceLocation(CLLocation)](/documentation/geotoolbox/placedescriptor/placerepresentation/devicelocation(_:))
- [PlaceDescriptor.SupportingPlaceRepresentation](/documentation/geotoolbox/placedescriptor/supportingplacerepresentation)

### Getting available supporting representations

- [case serviceIdentifiers([String : String])](/documentation/geotoolbox/placedescriptor/supportingplacerepresentation/serviceidentifiers(_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
