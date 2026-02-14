# QuickTime File Format Documentation

Source: https://sosumi.ai/documentation/quicktime-file-format

---
title: QuickTime File Format
source: https://developer.apple.com/documentation/quicktime-file-format
timestamp: 2026-02-13T19:34:34.494Z
---

## Essentials

- [Storing and sharing media with QuickTime files](/documentation/quicktime-file-format/storing_and_sharing_media_with_quicktime_files)

### Building in QuickTime

- [Atoms](/documentation/quicktime-file-format/atoms)
- [QT atoms and atom containers](/documentation/quicktime-file-format/qt_atoms_and_atom_containers)
- [Creating, copying, and disposing of atom containers](/documentation/quicktime-file-format/creating_copying_and_disposing_of_atom_containers)

#### Managing atoms

- [Creating new atoms](/documentation/quicktime-file-format/creating_new_atoms)
- [Copying existing atoms](/documentation/quicktime-file-format/copying_existing_atoms)
- [Retrieving atoms from an atom container](/documentation/quicktime-file-format/retrieving_atoms_from_an_atom_container)
- [Modifying atoms](/documentation/quicktime-file-format/modifying_atoms)
- [Removing atoms from an atom container](/documentation/quicktime-file-format/removing_atoms_from_an_atom_container)
- [QuickTime movie files](/documentation/quicktime-file-format/quicktime_movie_files)

#### Declaring compatibility

- [File type compatibility atom ('ftyp')](/documentation/quicktime-file-format/file_type_compatibility_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/file_type_compatibility_atom/size)
- [Type](/documentation/quicktime-file-format/file_type_compatibility_atom/type)
- [Major brand](/documentation/quicktime-file-format/file_type_compatibility_atom/major_brand)
- [Minor version](/documentation/quicktime-file-format/file_type_compatibility_atom/minor_version)
- [Compatible brands](/documentation/quicktime-file-format/file_type_compatibility_atom/compatible_brands)

#### Setting free space

- [Free space atom ('free')](/documentation/quicktime-file-format/free_space_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/free_space_atom/size)
- [Type](/documentation/quicktime-file-format/free_space_atom/type)
- [Free space](/documentation/quicktime-file-format/free_space_atom/free_space)
- [Skip atom ('skip')](/documentation/quicktime-file-format/skip_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/skip_atom/size)
- [Type](/documentation/quicktime-file-format/skip_atom/type)
- [Free space](/documentation/quicktime-file-format/skip_atom/free_space)
- [Wide atom ('wide')](/documentation/quicktime-file-format/wide_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/wide_atom/size)
- [Type](/documentation/quicktime-file-format/wide_atom/type)

#### Describing movie data

- [Movie data atom ('mdat')](/documentation/quicktime-file-format/movie_data_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/movie_data_atom/size)
- [Type](/documentation/quicktime-file-format/movie_data_atom/type)
- [Extended size](/documentation/quicktime-file-format/movie_data_atom/extended_size)
- [Movie media data](/documentation/quicktime-file-format/movie_data_atom/movie_media_data)

#### Describing preview information

- [Preview atom ('pnot')](/documentation/quicktime-file-format/preview_atom)

##### Atom fields

- [Size](/documentation/quicktime-file-format/preview_atom/size)
- [Type](/documentation/quicktime-file-format/preview_atom/type)
- [Modification date](/documentation/quicktime-file-format/preview_atom/modification_date)
- [Version number](/documentation/quicktime-file-format/preview_atom/version_number)
- [Atom type](/documentation/quicktime-file-format/preview_atom/atom_type)
- [Atom index](/documentation/quicktime-file-format/preview_atom/atom_index)

## Movies

- [Movie atoms](/documentation/quicktime-file-format/movie_atoms)

### Describing movies

- [Movie atom ('moov')](/documentation/quicktime-file-format/movie_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/movie_atom/size)
- [Type](/documentation/quicktime-file-format/movie_atom/type)
- [Profile atom](/documentation/quicktime-file-format/movie_atom/profile_atom)
- [Movie header atom](/documentation/quicktime-file-format/movie_atom/movie_header_atom)
- [Movie clipping atom](/documentation/quicktime-file-format/movie_atom/movie_clipping_atom)
- [Track atoms](/documentation/quicktime-file-format/movie_atom/track_atoms)
- [User data atom](/documentation/quicktime-file-format/movie_atom/user_data_atom)
- [Color table atom](/documentation/quicktime-file-format/movie_atom/color_table_atom)
- [Compressed movie atom](/documentation/quicktime-file-format/movie_atom/compressed_movie_atom)
- [Reference movie atom](/documentation/quicktime-file-format/movie_atom/reference_movie_atom)
- [Movie header atom ('mvhd')](/documentation/quicktime-file-format/movie_header_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/movie_header_atom/size)
- [Type](/documentation/quicktime-file-format/movie_header_atom/type)
- [Version](/documentation/quicktime-file-format/movie_header_atom/version)
- [Flags](/documentation/quicktime-file-format/movie_header_atom/flags)
- [Creation time](/documentation/quicktime-file-format/movie_header_atom/creation_time)
- [Modification time](/documentation/quicktime-file-format/movie_header_atom/modification_time)
- [Time scale](/documentation/quicktime-file-format/movie_header_atom/time_scale)
- [Duration](/documentation/quicktime-file-format/movie_header_atom/duration)
- [Preferred rate](/documentation/quicktime-file-format/movie_header_atom/preferred_rate)
- [Preferred volume](/documentation/quicktime-file-format/movie_header_atom/preferred_volume)
- [Reserved](/documentation/quicktime-file-format/movie_header_atom/reserved)
- [Matrix structure](/documentation/quicktime-file-format/movie_header_atom/matrix_structure)
- [Preview time](/documentation/quicktime-file-format/movie_header_atom/preview_time)
- [Preview duration](/documentation/quicktime-file-format/movie_header_atom/preview_duration)
- [Poster time](/documentation/quicktime-file-format/movie_header_atom/poster_time)
- [Selection time](/documentation/quicktime-file-format/movie_header_atom/selection_time)
- [Selection duration](/documentation/quicktime-file-format/movie_header_atom/selection_duration)
- [Current time](/documentation/quicktime-file-format/movie_header_atom/current_time)
- [Next track ID](/documentation/quicktime-file-format/movie_header_atom/next_track_id)
- [Color table atom ('ctab')](/documentation/quicktime-file-format/color_table_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/color_table_atom/size)
- [Type](/documentation/quicktime-file-format/color_table_atom/type)
- [Color table seed](/documentation/quicktime-file-format/color_table_atom/color_table_seed)
- [Color table flags](/documentation/quicktime-file-format/color_table_atom/color_table_flags)
- [Color table size](/documentation/quicktime-file-format/color_table_atom/color_table_size)
- [Color array](/documentation/quicktime-file-format/color_table_atom/color_array)
- [User data atoms](/documentation/quicktime-file-format/user_data_atoms)

#### Atoms for user data

- [User data atom ('udta')](/documentation/quicktime-file-format/user_data_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/user_data_atom/size)
- [Type](/documentation/quicktime-file-format/user_data_atom/type)
- [User data list](/documentation/quicktime-file-format/user_data_atom/user_data_list)
- [Track name atom ('tnam')](/documentation/quicktime-file-format/track_name_atom)

##### Data fields

- [Reserved](/documentation/quicktime-file-format/track_name_atom/reserved)
- [Language](/documentation/quicktime-file-format/track_name_atom/language)
- [Name](/documentation/quicktime-file-format/track_name_atom/name)
- [Print to video atom ('ptv ')](/documentation/quicktime-file-format/print_to_video_atom)

##### Data fields

- [Display size](/documentation/quicktime-file-format/print_to_video_atom/display_size)
- [Reserved](/documentation/quicktime-file-format/print_to_video_atom/reserved1)
- [Reserved](/documentation/quicktime-file-format/print_to_video_atom/reserved2)
- [Play on open](/documentation/quicktime-file-format/print_to_video_atom/play_on_open)
- [Interleaving movie data](/documentation/quicktime-file-format/interleaving_movie_data)
- [Track atoms](/documentation/quicktime-file-format/track_atoms)

### Describing tracks

- [Track atom ('trak')](/documentation/quicktime-file-format/track_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/track_atom/size)
- [Type](/documentation/quicktime-file-format/track_atom/type)
- [Track profile atom](/documentation/quicktime-file-format/track_atom/track_profile_atom)
- [Track header atom](/documentation/quicktime-file-format/track_atom/track_header_atom)
- [Track aperture mode dimensions atom](/documentation/quicktime-file-format/track_atom/track_aperture_mode_dimensions_atom)
- [Clipping atom](/documentation/quicktime-file-format/track_atom/clipping_atom)
- [Track matte atom](/documentation/quicktime-file-format/track_atom/track_matte_atom)
- [Edit atom](/documentation/quicktime-file-format/track_atom/edit_atom)
- [Track reference atom](/documentation/quicktime-file-format/track_atom/track_reference_atom)
- [Track exclude from autoselection atom](/documentation/quicktime-file-format/track_atom/track_exclude_from_autoselection_atom)
- [Track load settings atom](/documentation/quicktime-file-format/track_atom/track_load_settings_atom)
- [Track input map atom](/documentation/quicktime-file-format/track_atom/track_input_map_atom)
- [Media atom](/documentation/quicktime-file-format/track_atom/media_atom)
- [User-defined data atom](/documentation/quicktime-file-format/track_atom/user-defined_data_atom)
- [Track header atom ('tkhd')](/documentation/quicktime-file-format/track_header_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/track_header_atom/size)
- [Type](/documentation/quicktime-file-format/track_header_atom/type)
- [Version](/documentation/quicktime-file-format/track_header_atom/version)
- [Flags](/documentation/quicktime-file-format/track_header_atom/flags)
- [Creation time](/documentation/quicktime-file-format/track_header_atom/creation_time)
- [Modification time](/documentation/quicktime-file-format/track_header_atom/modification_time)
- [Track ID](/documentation/quicktime-file-format/track_header_atom/track_id)
- [Reserved](/documentation/quicktime-file-format/track_header_atom/reserved)
- [Duration](/documentation/quicktime-file-format/track_header_atom/duration)
- [Reserved](/documentation/quicktime-file-format/track_header_atom/reserved_2)
- [Layer](/documentation/quicktime-file-format/track_header_atom/layer)
- [Alternate group](/documentation/quicktime-file-format/track_header_atom/alternate_group)
- [Volume](/documentation/quicktime-file-format/track_header_atom/volume)
- [Reserved](/documentation/quicktime-file-format/track_header_atom/reserved_3)
- [Matrix structure](/documentation/quicktime-file-format/track_header_atom/matrix_structure)
- [Track width](/documentation/quicktime-file-format/track_header_atom/track_width)
- [Track height](/documentation/quicktime-file-format/track_header_atom/track_height)
- [Track exclude from autoselection atom ('txas')](/documentation/quicktime-file-format/track_exclude_from_autoselection_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/track_exclude_from_autoselection_atom/size)
- [Type](/documentation/quicktime-file-format/track_exclude_from_autoselection_atom/type)
- [Track aperture mode dimension atoms](/documentation/quicktime-file-format/track_aperture_mode_dimension_atoms)

#### Track aperture mode dimension atoms

- [Track aperture mode dimensions atom ('tapt')](/documentation/quicktime-file-format/track_aperture_mode_dimensions_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/track_aperture_mode_dimensions_atom/size)
- [Type](/documentation/quicktime-file-format/track_aperture_mode_dimensions_atom/type)
- [Track clean aperture dimensions atom](/documentation/quicktime-file-format/track_aperture_mode_dimensions_atom/track_clean_aperture_dimensions_atom)
- [Track production aperture dimensions atom](/documentation/quicktime-file-format/track_aperture_mode_dimensions_atom/track_production_aperture_dimensions_atom)
- [Track encoded pixels dimensions atom](/documentation/quicktime-file-format/track_aperture_mode_dimensions_atom/track_encoded_pixels_dimensions_atom)
- [Track clean aperture dimensions atom ('clef')](/documentation/quicktime-file-format/track_clean_aperture_dimensions_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/track_clean_aperture_dimensions_atom/size)
- [Type](/documentation/quicktime-file-format/track_clean_aperture_dimensions_atom/type)
- [Version](/documentation/quicktime-file-format/track_clean_aperture_dimensions_atom/version)
- [Flags](/documentation/quicktime-file-format/track_clean_aperture_dimensions_atom/flags)
- [Width](/documentation/quicktime-file-format/track_clean_aperture_dimensions_atom/width)
- [Height](/documentation/quicktime-file-format/track_clean_aperture_dimensions_atom/height)
- [Track production aperture dimensions atom ('prof')](/documentation/quicktime-file-format/track_production_aperture_dimensions_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/track_production_aperture_dimensions_atom/size)
- [Type](/documentation/quicktime-file-format/track_production_aperture_dimensions_atom/type)
- [Version](/documentation/quicktime-file-format/track_production_aperture_dimensions_atom/version)
- [Flags](/documentation/quicktime-file-format/track_production_aperture_dimensions_atom/flags)
- [Width](/documentation/quicktime-file-format/track_production_aperture_dimensions_atom/width)
- [Height](/documentation/quicktime-file-format/track_production_aperture_dimensions_atom/height)
- [Track encoded pixels dimensions atom ('enof')](/documentation/quicktime-file-format/track_encoded_pixels_dimensions_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/track_encoded_pixels_dimensions_atom/size)
- [Type](/documentation/quicktime-file-format/track_encoded_pixels_dimensions_atom/type)
- [Version](/documentation/quicktime-file-format/track_encoded_pixels_dimensions_atom/version)
- [Flags](/documentation/quicktime-file-format/track_encoded_pixels_dimensions_atom/flags)
- [Width](/documentation/quicktime-file-format/track_encoded_pixels_dimensions_atom/width)
- [Height](/documentation/quicktime-file-format/track_encoded_pixels_dimensions_atom/height)
- [Clipping atom ('clip')](/documentation/quicktime-file-format/clipping_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/clipping_atom/size)
- [Type](/documentation/quicktime-file-format/clipping_atom/type)
- [Clipping region atom](/documentation/quicktime-file-format/clipping_atom/clipping_region_atom)
- [Clipping region atom ('crgn')](/documentation/quicktime-file-format/clipping_region_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/clipping_region_atom/size)
- [Type](/documentation/quicktime-file-format/clipping_region_atom/type)
- [Region size](/documentation/quicktime-file-format/clipping_region_atom/region_size)
- [Region boundary box](/documentation/quicktime-file-format/clipping_region_atom/region_boundary_box)
- [Clipping region data](/documentation/quicktime-file-format/clipping_region_atom/clipping_region_data)
- [Track matte atom ('matt')](/documentation/quicktime-file-format/track_matte_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/track_matte_atom/size)
- [Type](/documentation/quicktime-file-format/track_matte_atom/type)
- [Compressed matte atom](/documentation/quicktime-file-format/track_matte_atom/compressed_matte_atom)
- [Compressed matte atom ('kmat')](/documentation/quicktime-file-format/compressed_matte_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/compressed_matte_atom/size)
- [Type](/documentation/quicktime-file-format/compressed_matte_atom/type)
- [Version](/documentation/quicktime-file-format/compressed_matte_atom/version)
- [Flags](/documentation/quicktime-file-format/compressed_matte_atom/flags)
- [Matte image description structure](/documentation/quicktime-file-format/compressed_matte_atom/matte_image_description_structure)
- [Matte data](/documentation/quicktime-file-format/compressed_matte_atom/matte_data)
- [Edit atom ('edts')](/documentation/quicktime-file-format/edit_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/edit_atom/size)
- [Type](/documentation/quicktime-file-format/edit_atom/type)
- [Edit list atom](/documentation/quicktime-file-format/edit_atom/edit_list_atom)
- [Edit list atom ('elst')](/documentation/quicktime-file-format/edit_list_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/edit_list_atom/size)
- [Type](/documentation/quicktime-file-format/edit_list_atom/type)
- [Version](/documentation/quicktime-file-format/edit_list_atom/version)
- [Flags](/documentation/quicktime-file-format/edit_list_atom/flags)
- [Number of entries](/documentation/quicktime-file-format/edit_list_atom/number_of_entries)
- [Edit list table](/documentation/quicktime-file-format/edit_list_atom/edit_list_table)
- [Playing with edit lists](/documentation/quicktime-file-format/playing_with_edit_lists)
- [Track load settings atom ('load')](/documentation/quicktime-file-format/track_load_settings_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/track_load_settings_atom/size)
- [Type](/documentation/quicktime-file-format/track_load_settings_atom/type)
- [Preload start time](/documentation/quicktime-file-format/track_load_settings_atom/preload_start_time)
- [Preload duration](/documentation/quicktime-file-format/track_load_settings_atom/preload_duration)
- [Preload flags](/documentation/quicktime-file-format/track_load_settings_atom/preload_flags)
- [Default hints](/documentation/quicktime-file-format/track_load_settings_atom/default_hints)
- [Track reference atoms](/documentation/quicktime-file-format/track_reference_atoms)

#### Atoms for track references

- [Track reference atom ('tref')](/documentation/quicktime-file-format/track_reference_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/track_reference_atom/size)
- [Type](/documentation/quicktime-file-format/track_reference_atom/type)
- [Track reference type atom](/documentation/quicktime-file-format/track_reference_atom/track_reference_type_atom)
- [Track reference type atom](/documentation/quicktime-file-format/track_reference_type_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/track_reference_type_atom/size)
- [Type](/documentation/quicktime-file-format/track_reference_type_atom/type)
- [Track IDs](/documentation/quicktime-file-format/track_reference_type_atom/track_ids)
- [Track input map atoms](/documentation/quicktime-file-format/track_input_map_atoms)

#### Atoms for track input

- [Track input map atom ('imap')](/documentation/quicktime-file-format/track_input_map_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/track_input_map_atom/size)
- [Type](/documentation/quicktime-file-format/track_input_map_atom/type)
- [Track input atoms](/documentation/quicktime-file-format/track_input_map_atom/track_input_atoms)
- [Track input atom ('  in')](/documentation/quicktime-file-format/track_input_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/track_input_atom/size)
- [Type](/documentation/quicktime-file-format/track_input_atom/type)
- [Atom ID](/documentation/quicktime-file-format/track_input_atom/atom_id)
- [Reserved](/documentation/quicktime-file-format/track_input_atom/reserved)
- [Child count](/documentation/quicktime-file-format/track_input_atom/child_count)
- [Reserved](/documentation/quicktime-file-format/track_input_atom/reserved_2)
- [Input type atom](/documentation/quicktime-file-format/track_input_atom/input_type_atom)
- [Object ID atom](/documentation/quicktime-file-format/track_input_atom/object_id_atom)
- [Input type atom ('  ty')](/documentation/quicktime-file-format/input_type_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/input_type_atom/size)
- [Type](/documentation/quicktime-file-format/input_type_atom/type)
- [Input type](/documentation/quicktime-file-format/input_type_atom/input_type)
- [Object ID atom ('obid')](/documentation/quicktime-file-format/object_id_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/object_id_atom/size)
- [Type](/documentation/quicktime-file-format/object_id_atom/type)
- [Object ID](/documentation/quicktime-file-format/object_id_atom/object_id)
- [Media atoms](/documentation/quicktime-file-format/media_atoms)

### Describing media

- [Media atom ('mdia')](/documentation/quicktime-file-format/media_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/media_atom/size)
- [Type](/documentation/quicktime-file-format/media_atom/type)
- [Media header atom](/documentation/quicktime-file-format/media_atom/media_header_atom)
- [Extended language tag atom](/documentation/quicktime-file-format/media_atom/extended_language_tag_atom)
- [Handler reference atom](/documentation/quicktime-file-format/media_atom/handler_reference_atom)
- [Media information atom](/documentation/quicktime-file-format/media_atom/media_information_atom)
- [User data atom](/documentation/quicktime-file-format/media_atom/user_data_atom)
- [Media header atom ('mdhd')](/documentation/quicktime-file-format/media_header_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/media_header_atom/size)
- [Type](/documentation/quicktime-file-format/media_header_atom/type)
- [Version](/documentation/quicktime-file-format/media_header_atom/version)
- [Flags](/documentation/quicktime-file-format/media_header_atom/flags)
- [Creation time](/documentation/quicktime-file-format/media_header_atom/creation_time)
- [Modification time](/documentation/quicktime-file-format/media_header_atom/modification_time)
- [Time scale](/documentation/quicktime-file-format/media_header_atom/time_scale)
- [Duration](/documentation/quicktime-file-format/media_header_atom/duration)
- [Language](/documentation/quicktime-file-format/media_header_atom/language)
- [Quality](/documentation/quicktime-file-format/media_header_atom/quality)
- [Extended language tag atom ('elng')](/documentation/quicktime-file-format/extended_language_tag_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/extended_language_tag_atom/size)
- [Type](/documentation/quicktime-file-format/extended_language_tag_atom/type)
- [Version](/documentation/quicktime-file-format/extended_language_tag_atom/version)
- [Flags](/documentation/quicktime-file-format/extended_language_tag_atom/flags)
- [Language tag string](/documentation/quicktime-file-format/extended_language_tag_atom/language_tag_string)
- [Handler reference atom ('hdlr')](/documentation/quicktime-file-format/handler_reference_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/handler_reference_atom/size)
- [Type](/documentation/quicktime-file-format/handler_reference_atom/type)
- [Version](/documentation/quicktime-file-format/handler_reference_atom/version)
- [Flags](/documentation/quicktime-file-format/handler_reference_atom/flags)
- [Component type](/documentation/quicktime-file-format/handler_reference_atom/component_type)
- [Component subtype](/documentation/quicktime-file-format/handler_reference_atom/component_subtype)
- [Component manufacturer](/documentation/quicktime-file-format/handler_reference_atom/component_manufacturer)
- [Component flags](/documentation/quicktime-file-format/handler_reference_atom/component_flags)
- [Component flags mask](/documentation/quicktime-file-format/handler_reference_atom/component_flags_mask)
- [Component name](/documentation/quicktime-file-format/handler_reference_atom/component_name)
- [Media information atoms](/documentation/quicktime-file-format/media_information_atoms)
- [Video media information atom ('minf')](/documentation/quicktime-file-format/video_media_information_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/video_media_information_atom/size)
- [Type](/documentation/quicktime-file-format/video_media_information_atom/type)
- [Video media information header atom](/documentation/quicktime-file-format/video_media_information_atom/video_media_information_header_atom)
- [Handler reference atom](/documentation/quicktime-file-format/video_media_information_atom/handler_reference_atom)
- [Data information atom](/documentation/quicktime-file-format/video_media_information_atom/data_information_atom)
- [Sample table atom](/documentation/quicktime-file-format/video_media_information_atom/sample_table_atom)
- [Video media information header atom ('vmhd')](/documentation/quicktime-file-format/video_media_information_header_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/video_media_information_header_atom/size)
- [Type](/documentation/quicktime-file-format/video_media_information_header_atom/type)
- [Version](/documentation/quicktime-file-format/video_media_information_header_atom/version)
- [Flags](/documentation/quicktime-file-format/video_media_information_header_atom/flags)
- [Graphics mode](/documentation/quicktime-file-format/video_media_information_header_atom/graphics_mode)
- [Opcolor](/documentation/quicktime-file-format/video_media_information_header_atom/opcolor)
- [Sound media information atom ('minf')](/documentation/quicktime-file-format/sound_media_information_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/sound_media_information_atom/size)
- [Type](/documentation/quicktime-file-format/sound_media_information_atom/type)
- [Sound media information header atom](/documentation/quicktime-file-format/sound_media_information_atom/sound_media_information_header_atom)
- [Handler reference atom](/documentation/quicktime-file-format/sound_media_information_atom/handler_reference_atom)
- [Data information atom](/documentation/quicktime-file-format/sound_media_information_atom/data_information_atom)
- [Sample table atom](/documentation/quicktime-file-format/sound_media_information_atom/sample_table_atom)
- [Sound media information header atom ('smhd')](/documentation/quicktime-file-format/sound_media_information_header_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/sound_media_information_header_atom/size)
- [Type](/documentation/quicktime-file-format/sound_media_information_header_atom/type)
- [Version](/documentation/quicktime-file-format/sound_media_information_header_atom/version)
- [Flags](/documentation/quicktime-file-format/sound_media_information_header_atom/flags)
- [Balance](/documentation/quicktime-file-format/sound_media_information_header_atom/balance)
- [Reserved](/documentation/quicktime-file-format/sound_media_information_header_atom/reserved)
- [Base media information atom ('minf')](/documentation/quicktime-file-format/base_media_information_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/base_media_information_atom/size)
- [Type](/documentation/quicktime-file-format/base_media_information_atom/type)
- [Base media information header atom](/documentation/quicktime-file-format/base_media_information_atom/base_media_information_header_atom)
- [Base media information header atom ('gmhd')](/documentation/quicktime-file-format/base_media_information_header_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/base_media_information_header_atom/size)
- [Type](/documentation/quicktime-file-format/base_media_information_header_atom/type)
- [Base media info atom](/documentation/quicktime-file-format/base_media_information_header_atom/base_media_info_atom)
- [Text media information atom](/documentation/quicktime-file-format/base_media_information_header_atom/text_media_information_atom)
- [Base media info atom ('gmin')](/documentation/quicktime-file-format/base_media_info_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/base_media_info_atom/size)
- [Type](/documentation/quicktime-file-format/base_media_info_atom/type)
- [Version](/documentation/quicktime-file-format/base_media_info_atom/version)
- [Flags](/documentation/quicktime-file-format/base_media_info_atom/flags)
- [Graphics mode](/documentation/quicktime-file-format/base_media_info_atom/graphics_mode)
- [Opcolor](/documentation/quicktime-file-format/base_media_info_atom/opcolor)
- [Balance](/documentation/quicktime-file-format/base_media_info_atom/balance)
- [Reserved](/documentation/quicktime-file-format/base_media_info_atom/reserved)
- [Data information atom ('dinf')](/documentation/quicktime-file-format/data_information_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/data_information_atom/size)
- [Type](/documentation/quicktime-file-format/data_information_atom/type)
- [Data reference atom](/documentation/quicktime-file-format/data_information_atom/data_reference_atom)
- [Data reference atom](/documentation/quicktime-file-format/media_data_reference_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/media_data_reference_atom/size)
- [Type](/documentation/quicktime-file-format/media_data_reference_atom/type)
- [Version](/documentation/quicktime-file-format/media_data_reference_atom/version)
- [Flags](/documentation/quicktime-file-format/media_data_reference_atom/flags)
- [Number of entries](/documentation/quicktime-file-format/media_data_reference_atom/number_of_entries)
- [Data references](/documentation/quicktime-file-format/media_data_reference_atom/data_references)
- [Sample atoms](/documentation/quicktime-file-format/sample_atoms)

### Describing samples

- [Sample table atom ('stbl')](/documentation/quicktime-file-format/sample_table_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/sample_table_atom/size)
- [Type](/documentation/quicktime-file-format/sample_table_atom/type)
- [Sample description atom](/documentation/quicktime-file-format/sample_table_atom/sample_description_atom)
- [Time-to-sample atom](/documentation/quicktime-file-format/sample_table_atom/time-to-sample_atom)
- [Composition offset atom](/documentation/quicktime-file-format/sample_table_atom/composition_offset_atom)
- [Composition shift least greatest atom](/documentation/quicktime-file-format/sample_table_atom/composition_shift_least_greatest_atom)
- [Sync sample atom](/documentation/quicktime-file-format/sample_table_atom/sync_sample_atom)
- [Partial sync sample atom](/documentation/quicktime-file-format/sample_table_atom/partial_sync_sample_atom)
- [Sample-to-chunk atom](/documentation/quicktime-file-format/sample_table_atom/sample-to-chunk_atom)
- [Sample size atom](/documentation/quicktime-file-format/sample_table_atom/sample_size_atom)
- [Chunk offset atom](/documentation/quicktime-file-format/sample_table_atom/chunk_offset_atom)
- [Sample dependency flags atom](/documentation/quicktime-file-format/sample_table_atom/sample_dependency_flags_atom)
- [Shadow sync atom](/documentation/quicktime-file-format/sample_table_atom/shadow_sync_atom)
- [Seeking with a QuickTime file](/documentation/quicktime-file-format/seeking_with_a_quicktime_file)
- [Sample description atom ('stsd')](/documentation/quicktime-file-format/sample_description_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/sample_description_atom/size)
- [Type](/documentation/quicktime-file-format/sample_description_atom/type)
- [Version](/documentation/quicktime-file-format/sample_description_atom/version)
- [Flags](/documentation/quicktime-file-format/sample_description_atom/flags)
- [Number of entries](/documentation/quicktime-file-format/sample_description_atom/number_of_entries)
- [Sample description table](/documentation/quicktime-file-format/sample_description_atom/sample_description_table)
- [Time-to-sample atom ('stts')](/documentation/quicktime-file-format/time-to-sample_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/time-to-sample_atom/size)
- [Type](/documentation/quicktime-file-format/time-to-sample_atom/type)
- [Version](/documentation/quicktime-file-format/time-to-sample_atom/version)
- [Flags](/documentation/quicktime-file-format/time-to-sample_atom/flags)
- [Number of entries](/documentation/quicktime-file-format/time-to-sample_atom/number_of_entries)
- [Time-to-sample table](/documentation/quicktime-file-format/time-to-sample_atom/time-to-sample_table)
- [Creating video tracks at 30 frames per second](/documentation/quicktime-file-format/creating_video_tracks_at_30_frames_per_second)
- [Creating video tracks at 29.97 frames per second](/documentation/quicktime-file-format/creating_video_tracks_at_2997_frames_per_second)
- [Creating sound tracks at 44.1 kHz](/documentation/quicktime-file-format/creating_sound_tracks_at_441_khz)
- [Composition offset atom ('ctts')](/documentation/quicktime-file-format/composition_offset_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/composition_offset_atom/size)
- [Type](/documentation/quicktime-file-format/composition_offset_atom/type)
- [Version](/documentation/quicktime-file-format/composition_offset_atom/version)
- [Flags](/documentation/quicktime-file-format/composition_offset_atom/flags)
- [Entry count](/documentation/quicktime-file-format/composition_offset_atom/entry_count)
- [Composition shift least greatest atom ('cslg')](/documentation/quicktime-file-format/composition_shift_least_greatest_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/composition_shift_least_greatest_atom/size)
- [Type](/documentation/quicktime-file-format/composition_shift_least_greatest_atom/type)
- [Version](/documentation/quicktime-file-format/composition_shift_least_greatest_atom/version)
- [Flags](/documentation/quicktime-file-format/composition_shift_least_greatest_atom/flags)
- [compositionOffsetToDisplayOffsetShift](/documentation/quicktime-file-format/composition_shift_least_greatest_atom/compositionoffsettodisplayoffsetshift)
- [leastDisplayOffset](/documentation/quicktime-file-format/composition_shift_least_greatest_atom/leastdisplayoffset)
- [greatestDisplayOffset](/documentation/quicktime-file-format/composition_shift_least_greatest_atom/greatestdisplayoffset)
- [displayStartTime](/documentation/quicktime-file-format/composition_shift_least_greatest_atom/displaystarttime)
- [displayEndTime](/documentation/quicktime-file-format/composition_shift_least_greatest_atom/displayendtime)
- [Using composition offset and composition shift least greatest atoms](/documentation/quicktime-file-format/using_composition_offset_and_composition_shift_least_greatest_atoms)
- [Sync sample atom ('stss')](/documentation/quicktime-file-format/sync_sample_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/sync_sample_atom/size)
- [Type](/documentation/quicktime-file-format/sync_sample_atom/type)
- [Version](/documentation/quicktime-file-format/sync_sample_atom/version)
- [Flags](/documentation/quicktime-file-format/sync_sample_atom/flags)
- [Number of entries](/documentation/quicktime-file-format/sync_sample_atom/number_of_entries)
- [Sync sample table](/documentation/quicktime-file-format/sync_sample_atom/sync_sample_table)
- [Partial sync sample atom ('stps')](/documentation/quicktime-file-format/partial_sync_sample_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/partial_sync_sample_atom/size)
- [Type](/documentation/quicktime-file-format/partial_sync_sample_atom/type)
- [Version](/documentation/quicktime-file-format/partial_sync_sample_atom/version)
- [Flags](/documentation/quicktime-file-format/partial_sync_sample_atom/flags)
- [Entry count](/documentation/quicktime-file-format/partial_sync_sample_atom/entry_count)
- [Partial sync sample table](/documentation/quicktime-file-format/partial_sync_sample_atom/partial_sync_sample_table)
- [Sample-to-chunk atom ('stsc')](/documentation/quicktime-file-format/sample-to-chunk_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/sample-to-chunk_atom/size)
- [Type](/documentation/quicktime-file-format/sample-to-chunk_atom/type)
- [Version](/documentation/quicktime-file-format/sample-to-chunk_atom/version)
- [Flags](/documentation/quicktime-file-format/sample-to-chunk_atom/flags)
- [Number of entries](/documentation/quicktime-file-format/sample-to-chunk_atom/number_of_entries)
- [Sample-to-chunk table](/documentation/quicktime-file-format/sample-to-chunk_atom/sample-to-chunk_table)
- [Referencing two data files with a single track](/documentation/quicktime-file-format/referencing_two_data_files_with_a_single_track)
- [Sample size atom ('stsz')](/documentation/quicktime-file-format/sample_size_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/sample_size_atom/size)
- [Type](/documentation/quicktime-file-format/sample_size_atom/type)
- [Version](/documentation/quicktime-file-format/sample_size_atom/version)
- [Flags](/documentation/quicktime-file-format/sample_size_atom/flags)
- [Sample size](/documentation/quicktime-file-format/sample_size_atom/sample_size)
- [Number of entries](/documentation/quicktime-file-format/sample_size_atom/number_of_entries)
- [Sample size table](/documentation/quicktime-file-format/sample_size_atom/sample_size_table)
- [Chunk offset atom ('stco')](/documentation/quicktime-file-format/chunk_offset_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/chunk_offset_atom/size)
- [Type](/documentation/quicktime-file-format/chunk_offset_atom/type)
- [Version](/documentation/quicktime-file-format/chunk_offset_atom/version)
- [Flags](/documentation/quicktime-file-format/chunk_offset_atom/flags)
- [Number of entries](/documentation/quicktime-file-format/chunk_offset_atom/number_of_entries)
- [Chunk offset table](/documentation/quicktime-file-format/chunk_offset_atom/chunk_offset_table)
- [Sample dependency flags atom ('sdtp')](/documentation/quicktime-file-format/sample_dependency_flags_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/sample_dependency_flags_atom/size)
- [Type](/documentation/quicktime-file-format/sample_dependency_flags_atom/type)
- [Version](/documentation/quicktime-file-format/sample_dependency_flags_atom/version)
- [Flags](/documentation/quicktime-file-format/sample_dependency_flags_atom/flags)
- [Sample dependency flags table](/documentation/quicktime-file-format/sample_dependency_flags_atom/sample_dependency_flags_table)
- [Using sample atoms](/documentation/quicktime-file-format/using_sample_atoms)
- [Structuring movie data and features](/documentation/quicktime-file-format/structuring_movie_data_and_features)

### Movie data

- [Compressed movie resources](/documentation/quicktime-file-format/compressed_movie_resources)
- [Reference movies](/documentation/quicktime-file-format/reference_movies)

#### Describing reference movies

- [Reference movie atom ('rmra')](/documentation/quicktime-file-format/reference_movie_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/reference_movie_atom/size)
- [Type](/documentation/quicktime-file-format/reference_movie_atom/type)
- [Reference movie descriptor atom](/documentation/quicktime-file-format/reference_movie_atom/reference_movie_descriptor_atom)
- [Reference movie descriptor atom ('rmda')](/documentation/quicktime-file-format/reference_movie_descriptor_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/reference_movie_descriptor_atom/size)
- [Type](/documentation/quicktime-file-format/reference_movie_descriptor_atom/type)
- [Data reference atom](/documentation/quicktime-file-format/reference_movie_descriptor_atom/data_reference_atom)
- [Data rate atom](/documentation/quicktime-file-format/reference_movie_descriptor_atom/data_rate_atom)
- [CPU speed atom](/documentation/quicktime-file-format/reference_movie_descriptor_atom/cpu_speed_atom)
- [Version check atom](/documentation/quicktime-file-format/reference_movie_descriptor_atom/version_check_atom)
- [Component detect atom](/documentation/quicktime-file-format/reference_movie_descriptor_atom/component_detect_atom)
- [Quality atom](/documentation/quicktime-file-format/reference_movie_descriptor_atom/quality_atom)
- [Data reference atom](/documentation/quicktime-file-format/reference_movie_data_reference_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/reference_movie_data_reference_atom/size)
- [Type](/documentation/quicktime-file-format/reference_movie_data_reference_atom/type)
- [Flags](/documentation/quicktime-file-format/reference_movie_data_reference_atom/flags)
- [Data reference type](/documentation/quicktime-file-format/reference_movie_data_reference_atom/data_reference_type)
- [Data reference size](/documentation/quicktime-file-format/reference_movie_data_reference_atom/data_reference_size)
- [Data reference](/documentation/quicktime-file-format/reference_movie_data_reference_atom/data_reference)
- [Data rate atom ('rmdr')](/documentation/quicktime-file-format/data_rate_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/data_rate_atom/size)
- [Type](/documentation/quicktime-file-format/data_rate_atom/type)
- [Flags](/documentation/quicktime-file-format/data_rate_atom/flags)
- [Data rate](/documentation/quicktime-file-format/data_rate_atom/data_rate)
- [CPU speed atom ('rmcs')](/documentation/quicktime-file-format/cpu_speed_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/cpu_speed_atom/size)
- [Type](/documentation/quicktime-file-format/cpu_speed_atom/type)
- [Flags](/documentation/quicktime-file-format/cpu_speed_atom/flags)
- [CPU speed](/documentation/quicktime-file-format/cpu_speed_atom/cpu_speed)
- [Version check atom ('rmvc')](/documentation/quicktime-file-format/version_check_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/version_check_atom/size)
- [Type](/documentation/quicktime-file-format/version_check_atom/type)
- [Flags](/documentation/quicktime-file-format/version_check_atom/flags)
- [Software package](/documentation/quicktime-file-format/version_check_atom/software_package)
- [Version](/documentation/quicktime-file-format/version_check_atom/version)
- [Mask](/documentation/quicktime-file-format/version_check_atom/mask)
- [Check type](/documentation/quicktime-file-format/version_check_atom/check_type)
- [Component detect atom ('rmcd')](/documentation/quicktime-file-format/component_detect_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/component_detect_atom/size)
- [Type](/documentation/quicktime-file-format/component_detect_atom/type)
- [Flags](/documentation/quicktime-file-format/component_detect_atom/flags)
- [Component description](/documentation/quicktime-file-format/component_detect_atom/component_description)
- [Minimum version](/documentation/quicktime-file-format/component_detect_atom/minimum_version)
- [Movie importer component flags](/documentation/quicktime-file-format/movie_importer_component_flags)
- [Quality atom ('rmqu')](/documentation/quicktime-file-format/quality_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/quality_atom/size)
- [Type](/documentation/quicktime-file-format/quality_atom/type)
- [Quality](/documentation/quicktime-file-format/quality_atom/quality)
- [Authoring movies with external movie targets](/documentation/quicktime-file-format/authoring_movies_with_external_movie_targets)

### Movie features

- [Preparing sound and subtitle alternate groups for use with Apple devices](/documentation/quicktime-file-format/preparing_sound_and_subtitle_alternate_groups_for_use_with_apple_devices)
- [Creating an effect description](/documentation/quicktime-file-format/creating_an_effect_description)

#### Effect descriptions

- [Structure of an effect description](/documentation/quicktime-file-format/structure_of_an_effect_description)
- [Required atoms of an effects description](/documentation/quicktime-file-format/required_atoms_of_an_effects_description)
- [Parameter atoms of an effects description](/documentation/quicktime-file-format/parameter_atoms_of_an_effects_description)
- [Creating an input map](/documentation/quicktime-file-format/creating_an_input_map)

## Metadata

- [Metadata atoms and types](/documentation/quicktime-file-format/metadata_atoms_and_types)

### Metadata structure

- [Metadata atom ('meta')](/documentation/quicktime-file-format/metadata_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/metadata_atom/size)
- [Type](/documentation/quicktime-file-format/metadata_atom/type)
- [Metadata handler atom](/documentation/quicktime-file-format/metadata_atom/metadata_handler_atom)
- [Metadata header atom](/documentation/quicktime-file-format/metadata_atom/metadata_header_atom)
- [Metadata item keys atom](/documentation/quicktime-file-format/metadata_atom/metadata_item_keys_atom)
- [Metadata item list atom](/documentation/quicktime-file-format/metadata_atom/metadata_item_list_atom)
- [Country list atom](/documentation/quicktime-file-format/metadata_atom/country_list_atom)
- [Language list atom](/documentation/quicktime-file-format/metadata_atom/language_list_atom)
- [Metadata handler atom ('hdlr')](/documentation/quicktime-file-format/metadata_handler_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/metadata_handler_atom/size)
- [Type](/documentation/quicktime-file-format/metadata_handler_atom/type)
- [Version](/documentation/quicktime-file-format/metadata_handler_atom/version)
- [Flags](/documentation/quicktime-file-format/metadata_handler_atom/flags)
- [Predefined](/documentation/quicktime-file-format/metadata_handler_atom/predefined)
- [Handler type](/documentation/quicktime-file-format/metadata_handler_atom/handler_type)
- [Reserved](/documentation/quicktime-file-format/metadata_handler_atom/reserved)
- [Name](/documentation/quicktime-file-format/metadata_handler_atom/name)
- [Metadata header atom ('mhdr')](/documentation/quicktime-file-format/metadata_header_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/metadata_header_atom/size)
- [Type](/documentation/quicktime-file-format/metadata_header_atom/type)
- [Version](/documentation/quicktime-file-format/metadata_header_atom/version)
- [Flags](/documentation/quicktime-file-format/metadata_header_atom/flags)
- [nextItemID](/documentation/quicktime-file-format/metadata_header_atom/nextitemid)

### Atoms

- [Country list atom ('ctry')](/documentation/quicktime-file-format/country_list_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/country_list_atom/size)
- [Type](/documentation/quicktime-file-format/country_list_atom/type)
- [Version](/documentation/quicktime-file-format/country_list_atom/version)
- [Flags](/documentation/quicktime-file-format/country_list_atom/flags)
- [Entry_count](/documentation/quicktime-file-format/country_list_atom/entry_count)
- [Country_count](/documentation/quicktime-file-format/country_list_atom/country_count)
- [Country_Country_count](/documentation/quicktime-file-format/country_list_atom/country_country_count)
- [Language list atom ('lang')](/documentation/quicktime-file-format/language_list_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/language_list_atom/size)
- [Type](/documentation/quicktime-file-format/language_list_atom/type)
- [Version](/documentation/quicktime-file-format/language_list_atom/version)
- [Flags](/documentation/quicktime-file-format/language_list_atom/flags)
- [Entry_count](/documentation/quicktime-file-format/language_list_atom/entry_count)
- [Language_count](/documentation/quicktime-file-format/language_list_atom/language_count)
- [Language_Language_count](/documentation/quicktime-file-format/language_list_atom/language_language_count)
- [Metadata item keys atom ('keys')](/documentation/quicktime-file-format/metadata_item_keys_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/metadata_item_keys_atom/size)
- [Type](/documentation/quicktime-file-format/metadata_item_keys_atom/type)
- [Version](/documentation/quicktime-file-format/metadata_item_keys_atom/version)
- [Flags](/documentation/quicktime-file-format/metadata_item_keys_atom/flags)
- [Entry_count](/documentation/quicktime-file-format/metadata_item_keys_atom/entry_count)
- [Key_size](/documentation/quicktime-file-format/metadata_item_keys_atom/key_size)
- [Key_namespace](/documentation/quicktime-file-format/metadata_item_keys_atom/key_namespace)
- [Key_value_Key_size-8](/documentation/quicktime-file-format/metadata_item_keys_atom/key_value_key_size-8)
- [Metadata item list atom ('ilst')](/documentation/quicktime-file-format/metadata_item_list_atom)

#### Data fields

- [Type](/documentation/quicktime-file-format/metadata_item_list_atom/type)
- [Item list](/documentation/quicktime-file-format/metadata_item_list_atom/item_list)
- [Metadata item atom](/documentation/quicktime-file-format/metadata_item_atom)

#### Data fields

- [Item_info](/documentation/quicktime-file-format/metadata_item_atom/item_info)
- [Name](/documentation/quicktime-file-format/metadata_item_atom/name)
- [Data value atom](/documentation/quicktime-file-format/metadata_item_atom/data_value_atom)
- [Value atom](/documentation/quicktime-file-format/value_atom)

#### Data fields

- [Type indicator](/documentation/quicktime-file-format/value_atom/type_indicator)
- [Locale indicator](/documentation/quicktime-file-format/value_atom/locale_indicator)
- [Item information atom ('itif')](/documentation/quicktime-file-format/item_information_atom)

#### Data fields

- [Size](/documentation/quicktime-file-format/item_information_atom/size)
- [Type](/documentation/quicktime-file-format/item_information_atom/type)
- [Version](/documentation/quicktime-file-format/item_information_atom/version)
- [Flags](/documentation/quicktime-file-format/item_information_atom/flags)
- [Item_ID](/documentation/quicktime-file-format/item_information_atom/item_id)
- [Name atom ('name')](/documentation/quicktime-file-format/name_atom)

#### Data fields

- [Version](/documentation/quicktime-file-format/name_atom/version)
- [Flags](/documentation/quicktime-file-format/name_atom/flags)
- [Name](/documentation/quicktime-file-format/name_atom/name)
- [Data atom ('data')](/documentation/quicktime-file-format/data_atom)

#### Data fields

- [Type indicator](/documentation/quicktime-file-format/data_atom/type_indicator)
- [Locale indicator](/documentation/quicktime-file-format/data_atom/locale_indicator)
- [Value](/documentation/quicktime-file-format/data_atom/value)

### Types and usage

- [Extensibility](/documentation/quicktime-file-format/extensibility)
- [Localization list sets](/documentation/quicktime-file-format/localization_list_sets)
- [Type indicator](/documentation/quicktime-file-format/type_indicator)
- [Locale indicator](/documentation/quicktime-file-format/locale_indicator)
- [Data ordering](/documentation/quicktime-file-format/data_ordering)
- [Well-known types](/documentation/quicktime-file-format/well-known_types)
- [Location metadata](/documentation/quicktime-file-format/location_metadata)
- [QuickTime metadata keys](/documentation/quicktime-file-format/quicktime_metadata_keys)
- [Direction definition](/documentation/quicktime-file-format/direction_definition)
- [Metadata handling](/documentation/quicktime-file-format/appendix_d_metadata_handling)

#### Handling metadata

- [Digital video file formats](/documentation/quicktime-file-format/digital_video_file_formats)
- [Digital audio file formats](/documentation/quicktime-file-format/digital_audio_file_formats)
- [Still image file formats](/documentation/quicktime-file-format/still_image_file_formats)
- [Animation and 3D file formats](/documentation/quicktime-file-format/animation_and_3d_file_formats)

## Media data

- [Media data atom types](/documentation/quicktime-file-format/media_data_atom_types)

### Video and sound

- [Video media](/documentation/quicktime-file-format/video_media)

#### Storing video data

- [Video sample description ('stsd')](/documentation/quicktime-file-format/video_sample_description)

##### Data fields

- [Sample description size](/documentation/quicktime-file-format/video_sample_description/sample_description_size)
- [Data format](/documentation/quicktime-file-format/video_sample_description/data_format)
- [Reserved](/documentation/quicktime-file-format/video_sample_description/reserved)
- [Data reference index](/documentation/quicktime-file-format/video_sample_description/data_reference_index)
- [Version](/documentation/quicktime-file-format/video_sample_description/version)
- [Revision level](/documentation/quicktime-file-format/video_sample_description/revision_level)
- [Vendor](/documentation/quicktime-file-format/video_sample_description/vendor)
- [Temporal quality](/documentation/quicktime-file-format/video_sample_description/temporal_quality)
- [Spatial quality](/documentation/quicktime-file-format/video_sample_description/spatial_quality)
- [Width](/documentation/quicktime-file-format/video_sample_description/width)
- [Height](/documentation/quicktime-file-format/video_sample_description/height)
- [Horizontal resolution](/documentation/quicktime-file-format/video_sample_description/horizontal_resolution)
- [Vertical resolution](/documentation/quicktime-file-format/video_sample_description/vertical_resolution)
- [Data size](/documentation/quicktime-file-format/video_sample_description/data_size)
- [Frame count](/documentation/quicktime-file-format/video_sample_description/frame_count)
- [Compressor name](/documentation/quicktime-file-format/video_sample_description/compressor_name)
- [Depth](/documentation/quicktime-file-format/video_sample_description/depth)
- [Color table ID](/documentation/quicktime-file-format/video_sample_description/color_table_id)
- [Video sample description extensions](/documentation/quicktime-file-format/video_sample_description_extensions)

##### Extending video sample descriptions

- [Pixel aspect ratio ('pasp')](/documentation/quicktime-file-format/pixel_aspect_ratio)

###### Data fields

- [Size](/documentation/quicktime-file-format/pixel_aspect_ratio/size)
- [Type](/documentation/quicktime-file-format/pixel_aspect_ratio/type)
- [hSpacing](/documentation/quicktime-file-format/pixel_aspect_ratio/hspacing)
- [vSpacing](/documentation/quicktime-file-format/pixel_aspect_ratio/vspacing)
- [MPEG-4 elementary stream descriptor atom ('esds')](/documentation/quicktime-file-format/mpeg-4_elementary_stream_descriptor_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/mpeg-4_elementary_stream_descriptor_atom/size)
- [Type](/documentation/quicktime-file-format/mpeg-4_elementary_stream_descriptor_atom/type)
- [Version](/documentation/quicktime-file-format/mpeg-4_elementary_stream_descriptor_atom/version)
- [Flags](/documentation/quicktime-file-format/mpeg-4_elementary_stream_descriptor_atom/flags)
- [Elementary stream descriptor](/documentation/quicktime-file-format/mpeg-4_elementary_stream_descriptor_atom/elementary_stream_descriptor)
- [AVC decoder configuration atom ('avcC')](/documentation/quicktime-file-format/avc_decoder_configuration_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/avc_decoder_configuration_atom/size)
- [Type](/documentation/quicktime-file-format/avc_decoder_configuration_atom/type)
- [AVC decoder configuration record](/documentation/quicktime-file-format/avc_decoder_configuration_atom/avc_decoder_configuration_record)
- [Color parameter atom ('colr')](/documentation/quicktime-file-format/color_parameter_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/color_parameter_atom/size)
- [Type](/documentation/quicktime-file-format/color_parameter_atom/type)
- [Color parameter type](/documentation/quicktime-file-format/color_parameter_atom/color_parameter_type)
- [Primaries index](/documentation/quicktime-file-format/color_parameter_atom/primaries_index)
- [Transfer function index](/documentation/quicktime-file-format/color_parameter_atom/transfer_function_index)
- [Matrix index](/documentation/quicktime-file-format/color_parameter_atom/matrix_index)
- [Clean aperture ('clap')](/documentation/quicktime-file-format/clean_aperture)

###### Data fields

- [Size](/documentation/quicktime-file-format/clean_aperture/size)
- [Type](/documentation/quicktime-file-format/clean_aperture/type)
- [apertureWidth_N](/documentation/quicktime-file-format/clean_aperture/aperturewidth_n)
- [apertureWidth_D](/documentation/quicktime-file-format/clean_aperture/aperturewidth_d)
- [apertureHeight_N](/documentation/quicktime-file-format/clean_aperture/apertureheight_n)
- [apertureHeight_D](/documentation/quicktime-file-format/clean_aperture/apertureheight_d)
- [horizOff_N](/documentation/quicktime-file-format/clean_aperture/horizoff_n)
- [horizOff_D](/documentation/quicktime-file-format/clean_aperture/horizoff_d)
- [vertOff_N](/documentation/quicktime-file-format/clean_aperture/vertoff_n)
- [vertOff_D](/documentation/quicktime-file-format/clean_aperture/vertoff_d)
- [Video sample data](/documentation/quicktime-file-format/video_sample_data)
- [Sound media](/documentation/quicktime-file-format/sound_media)

#### Storing audio data

- [Sound sample descriptions](/documentation/quicktime-file-format/sound_sample_descriptions)

##### Using sample descriptions

- [Sound sample description version 0 ('stsd')](/documentation/quicktime-file-format/sound_sample_description_version_0)

###### Data fields

- [Sample description size](/documentation/quicktime-file-format/sound_sample_description_version_0/sample_description_size)
- [Data format](/documentation/quicktime-file-format/sound_sample_description_version_0/data_format)
- [Reserved](/documentation/quicktime-file-format/sound_sample_description_version_0/reserved)
- [Data reference index](/documentation/quicktime-file-format/sound_sample_description_version_0/data_reference_index)
- [Version](/documentation/quicktime-file-format/sound_sample_description_version_0/version)
- [Revision level](/documentation/quicktime-file-format/sound_sample_description_version_0/revision_level)
- [Vendor](/documentation/quicktime-file-format/sound_sample_description_version_0/vendor)
- [Number of channels](/documentation/quicktime-file-format/sound_sample_description_version_0/number_of_channels)
- [Sample size](/documentation/quicktime-file-format/sound_sample_description_version_0/sample_size)
- [Compression ID](/documentation/quicktime-file-format/sound_sample_description_version_0/compression_id)
- [Packet size](/documentation/quicktime-file-format/sound_sample_description_version_0/packet_size)
- [Sample rate](/documentation/quicktime-file-format/sound_sample_description_version_0/sample_rate)
- [Sound sample description version 1 ('stsd')](/documentation/quicktime-file-format/sound_sample_description_version_1)

###### Data fields

- [Sample description size](/documentation/quicktime-file-format/sound_sample_description_version_1/sample_description_size)
- [Data format](/documentation/quicktime-file-format/sound_sample_description_version_1/data_format)
- [Reserved](/documentation/quicktime-file-format/sound_sample_description_version_1/reserved)
- [Data reference index](/documentation/quicktime-file-format/sound_sample_description_version_1/data_reference_index)
- [Version](/documentation/quicktime-file-format/sound_sample_description_version_1/version)
- [Revision level](/documentation/quicktime-file-format/sound_sample_description_version_1/revision_level)
- [Vendor](/documentation/quicktime-file-format/sound_sample_description_version_1/vendor)
- [Number of channels](/documentation/quicktime-file-format/sound_sample_description_version_1/number_of_channels)
- [Sample size](/documentation/quicktime-file-format/sound_sample_description_version_1/sample_size)
- [Compression ID](/documentation/quicktime-file-format/sound_sample_description_version_1/compression_id)
- [Packet size](/documentation/quicktime-file-format/sound_sample_description_version_1/packet_size)
- [Sample rate](/documentation/quicktime-file-format/sound_sample_description_version_1/sample_rate)
- [Samples per packet](/documentation/quicktime-file-format/sound_sample_description_version_1/samples_per_packet)
- [Bytes per packet](/documentation/quicktime-file-format/sound_sample_description_version_1/bytes_per_packet)
- [Bytes per frame](/documentation/quicktime-file-format/sound_sample_description_version_1/bytes_per_frame)
- [Bytes per sample](/documentation/quicktime-file-format/sound_sample_description_version_1/bytes_per_sample)
- [Sound sample description version 2 ('stsd')](/documentation/quicktime-file-format/sound_sample_description_version_2)

###### Data fields

- [Sample description size](/documentation/quicktime-file-format/sound_sample_description_version_2/sample_description_size)
- [Data format](/documentation/quicktime-file-format/sound_sample_description_version_2/data_format)
- [Reserved](/documentation/quicktime-file-format/sound_sample_description_version_2/reserved)
- [Data reference index](/documentation/quicktime-file-format/sound_sample_description_version_2/data_reference_index)
- [Version](/documentation/quicktime-file-format/sound_sample_description_version_2/version)
- [Revision level](/documentation/quicktime-file-format/sound_sample_description_version_2/revision_level)
- [Vendor](/documentation/quicktime-file-format/sound_sample_description_version_2/vendor)
- [always3](/documentation/quicktime-file-format/sound_sample_description_version_2/always3)
- [always16](/documentation/quicktime-file-format/sound_sample_description_version_2/always16)
- [alwaysMinus2](/documentation/quicktime-file-format/sound_sample_description_version_2/alwaysminus2)
- [always0](/documentation/quicktime-file-format/sound_sample_description_version_2/always0)
- [always65536](/documentation/quicktime-file-format/sound_sample_description_version_2/always65536)
- [sizeOfStructOnly](/documentation/quicktime-file-format/sound_sample_description_version_2/sizeofstructonly)
- [numAudioChannels](/documentation/quicktime-file-format/sound_sample_description_version_2/numaudiochannels)
- [always7F000000](/documentation/quicktime-file-format/sound_sample_description_version_2/always7f000000)
- [constBitsPerChannel](/documentation/quicktime-file-format/sound_sample_description_version_2/constbitsperchannel)
- [formatSpecificFlags](/documentation/quicktime-file-format/sound_sample_description_version_2/formatspecificflags)
- [constBytesPerAudioPacket](/documentation/quicktime-file-format/sound_sample_description_version_2/constbytesperaudiopacket)
- [constLPCMFramesPerAudioPacket](/documentation/quicktime-file-format/sound_sample_description_version_2/constlpcmframesperaudiopacket)
- [Sound sample description extensions](/documentation/quicktime-file-format/sound_sample_description_extensions)

##### Extending sound sample descriptions

- [siSlopeAndIntercept atom](/documentation/quicktime-file-format/sislopeandintercept_atom)

###### Data fields

- [Slope](/documentation/quicktime-file-format/sislopeandintercept_atom/slope)
- [Intercept](/documentation/quicktime-file-format/sislopeandintercept_atom/intercept)
- [minClip](/documentation/quicktime-file-format/sislopeandintercept_atom/minclip)
- [maxClip](/documentation/quicktime-file-format/sislopeandintercept_atom/maxclip)
- [siDecompressionParam atom ('wave')](/documentation/quicktime-file-format/sidecompressionparam_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/sidecompressionparam_atom/size)
- [Type](/documentation/quicktime-file-format/sidecompressionparam_atom/type)
- [Extension atoms](/documentation/quicktime-file-format/sidecompressionparam_atom/extension_atoms)
- [Format atom ('frma')](/documentation/quicktime-file-format/format_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/format_atom/size)
- [Type](/documentation/quicktime-file-format/format_atom/type)
- [Data format](/documentation/quicktime-file-format/format_atom/data_format)
- [Terminator atom ('0x00000000')](/documentation/quicktime-file-format/terminator_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/terminator_atom/size)
- [Type](/documentation/quicktime-file-format/terminator_atom/type)
- [MPEG-4 elementary stream descriptor atom  ('esds')](/documentation/quicktime-file-format/mpeg-4_elementary_sound_stream_descriptor_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/mpeg-4_elementary_sound_stream_descriptor_atom/size)
- [Type](/documentation/quicktime-file-format/mpeg-4_elementary_sound_stream_descriptor_atom/type)
- [Version](/documentation/quicktime-file-format/mpeg-4_elementary_sound_stream_descriptor_atom/version)
- [Elementary stream descriptor](/documentation/quicktime-file-format/mpeg-4_elementary_sound_stream_descriptor_atom/elementary_stream_descriptor)
- [Audio channel layout atom ('chan')](/documentation/quicktime-file-format/audio_channel_layout_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/audio_channel_layout_atom/size)
- [Type](/documentation/quicktime-file-format/audio_channel_layout_atom/type)
- [Version](/documentation/quicktime-file-format/audio_channel_layout_atom/version)
- [Flags](/documentation/quicktime-file-format/audio_channel_layout_atom/flags)
- [Audio channel layout](/documentation/quicktime-file-format/audio_channel_layout_atom/audio_channel_layout)
- [Subtitle follows track reference atom ('folw')](/documentation/quicktime-file-format/subtitle_follows_track_reference_atom)
- [Sound sample data](/documentation/quicktime-file-format/sound_sample_data)
- [Audio priming-handling encoder delay in AAC](/documentation/quicktime-file-format/appendix_g_audio_priming_handling_encoder_delay_in_aac)

##### Handling encoder delay

- [AAC encoding background](/documentation/quicktime-file-format/background_aac_encoding)
- [The timing and synchronization problem](/documentation/quicktime-file-format/the_timing_and_synchronization_problem)
- [Historical solution for implicit encoder delay](/documentation/quicktime-file-format/historical_solution_implicit_encoder_delay)
- [Using track structures to represent encoder delay explicitly](/documentation/quicktime-file-format/using_track_structures_to_represent_encode_delay_explictly)

###### Sample group structures

- [Sample group description atom ('sgpd')](/documentation/quicktime-file-format/sample_group_description_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/sample_group_description_atom/size)
- [Type](/documentation/quicktime-file-format/sample_group_description_atom/type)
- [Version](/documentation/quicktime-file-format/sample_group_description_atom/version)
- [Flags](/documentation/quicktime-file-format/sample_group_description_atom/flags)
- [Grouping type](/documentation/quicktime-file-format/sample_group_description_atom/grouping_type)
- [Default length](/documentation/quicktime-file-format/sample_group_description_atom/default_length)
- [Entry count](/documentation/quicktime-file-format/sample_group_description_atom/entry_count)
- [Payload data](/documentation/quicktime-file-format/sample_group_description_atom/payload_data)
- [Sample-to-group atom ('sbgp')](/documentation/quicktime-file-format/sample-to-group_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/sample-to-group_atom/size)
- [Type](/documentation/quicktime-file-format/sample-to-group_atom/type)
- [Version](/documentation/quicktime-file-format/sample-to-group_atom/version)
- [Flags](/documentation/quicktime-file-format/sample-to-group_atom/flags)
- [Grouping type](/documentation/quicktime-file-format/sample-to-group_atom/grouping_type)
- [Default length](/documentation/quicktime-file-format/sample-to-group_atom/default_length)
- [Entry count](/documentation/quicktime-file-format/sample-to-group_atom/entry_count)
- [Table data](/documentation/quicktime-file-format/sample-to-group_atom/table_data)
- [Representing encoder delay explicitly](/documentation/quicktime-file-format/example_representing_encoder_delay_explicitly)
- [Representing encoder delay with track structures](/documentation/quicktime-file-format/summary_using_track_structures_to_represent_encoder_delay)
- [Music media](/documentation/quicktime-file-format/music_media)
- [MPEG-1 media](/documentation/quicktime-file-format/mpeg-1_media)
- [Movie media](/documentation/quicktime-file-format/movie_media)

#### Storing embedded movies

- [Movie media sample](/documentation/quicktime-file-format/movie_media_sample)

##### Data fields

- [kMovieMediaDataReference](/documentation/quicktime-file-format/movie_media_sample/kmoviemediadatareference)
- [kMovieMediaDefaultDataReferenceID](/documentation/quicktime-file-format/movie_media_sample/kmoviemediadefaultdatareferenceid)
- [kMovieMediaAutoPlay](/documentation/quicktime-file-format/movie_media_sample/kmoviemediaautoplay)
- [kMovieMediaLoop](/documentation/quicktime-file-format/movie_media_sample/kmoviemedialoop)
- [kMovieMediaUseMIMEType](/documentation/quicktime-file-format/movie_media_sample/kmoviemediausemimetype)
- [kMovieMediaTitle](/documentation/quicktime-file-format/movie_media_sample/kmoviemediatitle)
- [kMovieMediaAltText](/documentation/quicktime-file-format/movie_media_sample/kmoviemediaalttext)
- [kMovieMediaClipBegin](/documentation/quicktime-file-format/movie_media_sample/kmoviemediaclipbegin)
- [kMovieMediaClipDuration](/documentation/quicktime-file-format/movie_media_sample/kmoviemediaclipduration)
- [kMovieMediaEnableFrameStepping](/documentation/quicktime-file-format/movie_media_sample/kmoviemediaenableframestepping)
- [kMovieMediaBackgroundColor](/documentation/quicktime-file-format/movie_media_sample/kmoviemediabackgroundcolor)
- [kMovieMediaRegionAtom](/documentation/quicktime-file-format/movie_media_sample/kmoviemediaregionatom)
- [kMovieMediaRectangleAtom](/documentation/quicktime-file-format/movie_media_sample/kmoviemediarectangleatom)
- [Defining media data layouts](/documentation/quicktime-file-format/appendix_b_defining_media_data_layouts)

#### Defining data layouts

- [Using QuickTime files and media layouts](/documentation/quicktime-file-format/using_quicktime_files_and_media_layouts)

### Time-specific media

- [Timed metadata media](/documentation/quicktime-file-format/timed_metadata_media)

#### Storing timed metadata media

- [Overview of timed metadata](/documentation/quicktime-file-format/overview_of_timed_metadata)
- [Timed metadata sample description](/documentation/quicktime-file-format/timed_metadata_sample_descriptions)

##### Describing timed metadata

- [Metadata key table atom ('keys')](/documentation/quicktime-file-format/metadata_key_table_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/metadata_key_table_atom/size)
- [Type](/documentation/quicktime-file-format/metadata_key_table_atom/type)
- [Metadata key table](/documentation/quicktime-file-format/metadata_key_table_atom/metadata_key_table)
- [Bit rate atom ('btrt')](/documentation/quicktime-file-format/bit_rate_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/bit_rate_atom/size)
- [Type](/documentation/quicktime-file-format/bit_rate_atom/type)
- [Buffer size](/documentation/quicktime-file-format/bit_rate_atom/buffer_size)
- [Max bit rate](/documentation/quicktime-file-format/bit_rate_atom/max_bit_rate)
- [Average bit rate](/documentation/quicktime-file-format/bit_rate_atom/average_bit_rate)
- [Metadata key atom](/documentation/quicktime-file-format/metadata_key_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/metadata_key_atom/size)
- [Type](/documentation/quicktime-file-format/metadata_key_atom/type)
- [Variable array of atoms](/documentation/quicktime-file-format/metadata_key_atom/variable_array_of_atoms)
- [Metadata key declaration atom ('keyd')](/documentation/quicktime-file-format/metadata_key_declaration_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/metadata_key_declaration_atom/size)
- [Type](/documentation/quicktime-file-format/metadata_key_declaration_atom/type)
- [Key_namespace](/documentation/quicktime-file-format/metadata_key_declaration_atom/key_namespace)
- [Key_value array](/documentation/quicktime-file-format/metadata_key_declaration_atom/key_value_array)
- [Metadata datatype definition atom ('dtyp')](/documentation/quicktime-file-format/metadata_datatype_definition_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/metadata_datatype_definition_atom/size)
- [Type](/documentation/quicktime-file-format/metadata_datatype_definition_atom/type)
- [Datatype namespace](/documentation/quicktime-file-format/metadata_datatype_definition_atom/datatype_namespace)
- [Datatype array](/documentation/quicktime-file-format/metadata_datatype_definition_atom/datatype_array)
- [Metadata locale atom ('loca')](/documentation/quicktime-file-format/metadata_locale_atom)

###### Data fields

- [Size](/documentation/quicktime-file-format/metadata_locale_atom/size)
- [Type](/documentation/quicktime-file-format/metadata_locale_atom/type)
- [Locale string](/documentation/quicktime-file-format/metadata_locale_atom/locale_string)
- [Timed metadata sample data format](/documentation/quicktime-file-format/timed_metadata_sample_data_format)
- [Constant-size timed metadata sample data](/documentation/quicktime-file-format/constant-size_timed_metadata_sample_data)
- [Combining multiple streams of metadata into the same track](/documentation/quicktime-file-format/combining_multiple_streams_of_metadata_into_the_same_track)
- [Movie-level relationships among tracks](/documentation/quicktime-file-format/movie-level_relationships_among_tracks)
- [Timecode media](/documentation/quicktime-file-format/timecode_media)

#### Storing time code data

- [Timecode sample description](/documentation/quicktime-file-format/timecode_sample_description)

##### Data fields

- [Reserved](/documentation/quicktime-file-format/timecode_sample_description/reserved)
- [Flags](/documentation/quicktime-file-format/timecode_sample_description/flags)
- [Time scale](/documentation/quicktime-file-format/timecode_sample_description/time_scale)
- [Frame duration](/documentation/quicktime-file-format/timecode_sample_description/frame_duration)
- [Number of frames](/documentation/quicktime-file-format/timecode_sample_description/number_of_frames)
- [Reserved](/documentation/quicktime-file-format/timecode_sample_description/reserved2)
- [Source reference](/documentation/quicktime-file-format/timecode_sample_description/source_reference)
- [Timecode media information atom ('tcmi')](/documentation/quicktime-file-format/timecode_media_information_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/timecode_media_information_atom/size)
- [Type](/documentation/quicktime-file-format/timecode_media_information_atom/type)
- [Version](/documentation/quicktime-file-format/timecode_media_information_atom/version)
- [Flags](/documentation/quicktime-file-format/timecode_media_information_atom/flags)
- [Text font](/documentation/quicktime-file-format/timecode_media_information_atom/text_font)
- [Text face](/documentation/quicktime-file-format/timecode_media_information_atom/text_face)
- [Text size](/documentation/quicktime-file-format/timecode_media_information_atom/text_size)
- [Reserved](/documentation/quicktime-file-format/timecode_media_information_atom/reserved)
- [Text color](/documentation/quicktime-file-format/timecode_media_information_atom/text_color)
- [Background color](/documentation/quicktime-file-format/timecode_media_information_atom/background_color)
- [Font name](/documentation/quicktime-file-format/timecode_media_information_atom/font_name)
- [Timecode sample data](/documentation/quicktime-file-format/timecode_sample_data)

##### Data fields

- [Hours](/documentation/quicktime-file-format/timecode_sample_data/hours)
- [Negative](/documentation/quicktime-file-format/timecode_sample_data/negative)
- [Minutes](/documentation/quicktime-file-format/timecode_sample_data/minutes)
- [Seconds](/documentation/quicktime-file-format/timecode_sample_data/seconds)
- [Frames](/documentation/quicktime-file-format/timecode_sample_data/frames)
- [Creating a timecode track for 29.97 FPS video](/documentation/quicktime-file-format/creating_a_timecode_track_for_2997_fps_video)

### Text, captions, and subtitles

- [Text media](/documentation/quicktime-file-format/text_media)

#### Storing text data

- [Text sample description](/documentation/quicktime-file-format/text_sample_description)

##### Data fields

- [Display flags](/documentation/quicktime-file-format/text_sample_description/display_flags)
- [Text justification](/documentation/quicktime-file-format/text_sample_description/text_justification)
- [Background color](/documentation/quicktime-file-format/text_sample_description/background_color)
- [Default text box](/documentation/quicktime-file-format/text_sample_description/default_text_box)
- [Reserved](/documentation/quicktime-file-format/text_sample_description/reserved)
- [Font number](/documentation/quicktime-file-format/text_sample_description/font_number)
- [Font face](/documentation/quicktime-file-format/text_sample_description/font_face)
- [Reserved](/documentation/quicktime-file-format/text_sample_description/reserved2)
- [Reserved](/documentation/quicktime-file-format/text_sample_description/reserved3)
- [Foreground color](/documentation/quicktime-file-format/text_sample_description/foreground_color)
- [Text name](/documentation/quicktime-file-format/text_sample_description/text_name)
- [Text media information atom ('text')](/documentation/quicktime-file-format/text_media_information_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/text_media_information_atom/size)
- [Type](/documentation/quicktime-file-format/text_media_information_atom/type)
- [Matrix structure](/documentation/quicktime-file-format/text_media_information_atom/matrix_structure)
- [Text sample data](/documentation/quicktime-file-format/text_sample_data)
- [Hypertext and wired text](/documentation/quicktime-file-format/hypertext_and_wired_text)
- [Closed captioning media](/documentation/quicktime-file-format/closed_captioning_media)

#### Storing closed captioning

- [Closed captioning sample description](/documentation/quicktime-file-format/closed_captioning_sample_description)
- [Closed captioning sample data ('cdat')](/documentation/quicktime-file-format/closed_captioning_sample_data)

##### Data fields

- [Size](/documentation/quicktime-file-format/closed_captioning_sample_data/size)
- [Type](/documentation/quicktime-file-format/closed_captioning_sample_data/type)
- [Sample data](/documentation/quicktime-file-format/closed_captioning_sample_data/sample_data)
- [Including multiple closed-caption tracks](/documentation/quicktime-file-format/including_multiple_closed-caption_tracks)
- [Subtitle media](/documentation/quicktime-file-format/subtitle_media)

#### Storing subtitles

- [Subtitle sample description](/documentation/quicktime-file-format/subtitle_sample_description)

##### Data fields

- [Display flags](/documentation/quicktime-file-format/subtitle_sample_description/display_flags)
- [Reserved](/documentation/quicktime-file-format/subtitle_sample_description/reserved)
- [Reserved](/documentation/quicktime-file-format/subtitle_sample_description/reserved2)
- [Reserved](/documentation/quicktime-file-format/subtitle_sample_description/reserved3)
- [Default text box](/documentation/quicktime-file-format/subtitle_sample_description/default_text_box)
- [Reserved](/documentation/quicktime-file-format/subtitle_sample_description/reserved4)
- [Font identifier](/documentation/quicktime-file-format/subtitle_sample_description/font_identifier)
- [Font face](/documentation/quicktime-file-format/subtitle_sample_description/font_face)
- [Font size](/documentation/quicktime-file-format/subtitle_sample_description/font_size)
- [Foreground color](/documentation/quicktime-file-format/subtitle_sample_description/foreground_color)
- [Font table](/documentation/quicktime-file-format/subtitle_sample_description/font_table)
- [Font table atom ('ftab')](/documentation/quicktime-file-format/font_table_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/font_table_atom/size)
- [Type](/documentation/quicktime-file-format/font_table_atom/type)
- [Count](/documentation/quicktime-file-format/font_table_atom/count)
- [Font identifier](/documentation/quicktime-file-format/font_table_atom/font_identifier)
- [Font name length](/documentation/quicktime-file-format/font_table_atom/font_name_length)
- [Font name](/documentation/quicktime-file-format/font_table_atom/font_name)
- [Subtitle sample data](/documentation/quicktime-file-format/subtitle_sample_data)

##### Data fields

- [Text size](/documentation/quicktime-file-format/subtitle_sample_data/text_size)
- [Text](/documentation/quicktime-file-format/subtitle_sample_data/text)
- [Sample extensions](/documentation/quicktime-file-format/subtitle_sample_data/sample_extensions)
- [Subtitle style atom ('styl')](/documentation/quicktime-file-format/subtitle_style_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/subtitle_style_atom/size)
- [Type](/documentation/quicktime-file-format/subtitle_style_atom/type)
- [Entry count](/documentation/quicktime-file-format/subtitle_style_atom/entry_count)
- [Subtitle text style record](/documentation/quicktime-file-format/subtitle_style_atom/subtitle_text_style_record)
- [Text box atom ('tbox')](/documentation/quicktime-file-format/text_box_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/text_box_atom/size)
- [Type](/documentation/quicktime-file-format/text_box_atom/type)
- [Text box](/documentation/quicktime-file-format/text_box_atom/text_box)
- [Subtitle track header size and placement](/documentation/quicktime-file-format/subtitle_track_header_size_and_placement)
- [Referencing a related forced subtitle track](/documentation/quicktime-file-format/referencing_a_related_forced_subtitle_track)

### Track features

- [Modifier tracks](/documentation/quicktime-file-format/modifier_tracks)
- [Creating movies with modifier tracks](/documentation/quicktime-file-format/creating_movies_with_modifier_tracks)
- [Track references](/documentation/quicktime-file-format/track_references)
- [Chapter lists](/documentation/quicktime-file-format/chapter_lists)
- [Streaming media](/documentation/quicktime-file-format/streaming_media)

### Hint media

- [Hint media](/documentation/quicktime-file-format/hint_media)
- [Finding an original media track from a hint track](/documentation/quicktime-file-format/finding_an_original_media_track_from_a_hint_track)
- [RTP hint tracks](/documentation/quicktime-file-format/rtp_hint_tracks)
- [Hint sample data format](/documentation/quicktime-file-format/hint_track_sample_description)

#### Data fields

- [Size](/documentation/quicktime-file-format/hint_track_sample_description/size)
- [Data format](/documentation/quicktime-file-format/hint_track_sample_description/data_format)
- [Reserved](/documentation/quicktime-file-format/hint_track_sample_description/reserved)
- [Data reference index](/documentation/quicktime-file-format/hint_track_sample_description/data_reference_index)
- [Hint track version](/documentation/quicktime-file-format/hint_track_sample_description/hint_track_version)
- [Last compatible hint track version](/documentation/quicktime-file-format/hint_track_sample_description/last_compatible_hint_track_version)
- [Max packet size](/documentation/quicktime-file-format/hint_track_sample_description/max_packet_size)
- [Additional data table](/documentation/quicktime-file-format/hint_track_sample_description/additional_data_table)
- [Packetization hint sample data](/documentation/quicktime-file-format/packetization_hint_sample_data)

#### Data fields

- [Entry count](/documentation/quicktime-file-format/packetization_hint_sample_data/entry_count)
- [Reserved](/documentation/quicktime-file-format/packetization_hint_sample_data/reserved)
- [Packet entry table](/documentation/quicktime-file-format/packetization_hint_sample_data/packet_entry_table)
- [Additional data](/documentation/quicktime-file-format/packetization_hint_sample_data/additional_data)

#### Packet entries

- [Packet entry](/documentation/quicktime-file-format/packet_entry)

##### Data fields

- [Relative packet transmission time](/documentation/quicktime-file-format/packet_entry/relative_packet_transmission_time)
- [RTP header info](/documentation/quicktime-file-format/packet_entry/rtp_header_info)
- [RTP sequence number](/documentation/quicktime-file-format/packet_entry/rtp_sequence_number)
- [Flags](/documentation/quicktime-file-format/packet_entry/flags)
- [Entry count](/documentation/quicktime-file-format/packet_entry/entry_count)
- [Extra information TLVs](/documentation/quicktime-file-format/packet_entry/extra_information_tlvs)
- [Data table](/documentation/quicktime-file-format/packet_entry/data_table)

#### Data modes

- [Data modes](/documentation/quicktime-file-format/data_modes)

## Data types

- [Basic QuickTime data types](/documentation/quicktime-file-format/basic_data_types)

### Languages

- [Language code values](/documentation/quicktime-file-format/language_code_values)

### Dates and times

- [Calendar date and time values](/documentation/quicktime-file-format/calendar_date_and_time_values)

### Graphics and colors

- [Matrices](/documentation/quicktime-file-format/matrices)
- [Graphics modes](/documentation/quicktime-file-format/graphics_modes)
- [RGB colors](/documentation/quicktime-file-format/rgb_colors)
- [Balance](/documentation/quicktime-file-format/balance)

## Change log

- [QuickTime File Format change log](/documentation/quicktime-file-format/revision_history)

## Deprecated

- [Deprecated atoms](/documentation/quicktime-file-format/deprecated_atoms)

### Movie atoms

- [Movie profile atom ('prfl')](/documentation/quicktime-file-format/movie_profile_atom)

#### Data fields

- [Reserved](/documentation/quicktime-file-format/movie_profile_atom/reserved)
- [Part-ID](/documentation/quicktime-file-format/movie_profile_atom/part-id)
- [Feature code](/documentation/quicktime-file-format/movie_profile_atom/feature_code)
- [Value](/documentation/quicktime-file-format/movie_profile_atom/value)
- [Track profile atom ('prfl')](/documentation/quicktime-file-format/track_profile_atom)

#### Data fields

- [Reserved](/documentation/quicktime-file-format/track_profile_atom/reserved)
- [Part-ID](/documentation/quicktime-file-format/track_profile_atom/part-id)
- [Feature code](/documentation/quicktime-file-format/track_profile_atom/feature_code)
- [Value](/documentation/quicktime-file-format/track_profile_atom/value)
- [Appendix F: Profile atom guidelines](/documentation/quicktime-file-format/appendix_f_profile_atom_guidelines)

#### Building a profile atom

- [About this appendix](/documentation/quicktime-file-format/about_this_appendix)
- [Profile atom ('prfl')](/documentation/quicktime-file-format/profile_atom)

##### Data fields

- [Size](/documentation/quicktime-file-format/profile_atom/size)
- [Type](/documentation/quicktime-file-format/profile_atom/type)
- [Version](/documentation/quicktime-file-format/profile_atom/version)
- [Flags](/documentation/quicktime-file-format/profile_atom/flags)
- [Number of feature entries](/documentation/quicktime-file-format/profile_atom/number_of_feature_entries)
- [Feature entries](/documentation/quicktime-file-format/profile_atom/feature_entries)
- [Universal features](/documentation/quicktime-file-format/universal_features)

##### Setting features

- [Table of features](/documentation/quicktime-file-format/table_of_features)
- [Maximum video bit rate](/documentation/quicktime-file-format/maximum_video_bit_rate)
- [Average video bit rate](/documentation/quicktime-file-format/average_video_bit_rate)
- [Maximum audio bit rate](/documentation/quicktime-file-format/maximum_audio_bit_rate)
- [Average audio bit rate](/documentation/quicktime-file-format/average_audio_bit_rate)
- [QuickTime video codec type](/documentation/quicktime-file-format/quicktime_video_codec_type)
- [QuickTime audio codec type](/documentation/quicktime-file-format/quicktime_audio_codec_type)
- [MPEG-4 video profile](/documentation/quicktime-file-format/mpeg-4_video_profile)
- [MPEG-4 video codec](/documentation/quicktime-file-format/mpeg-4_video_codec)
- [MPEG-4 video object type](/documentation/quicktime-file-format/mpeg-4_video_object_type)
- [MPEG-4 audio codec](/documentation/quicktime-file-format/mpeg-4_audio_codec)
- [Maximum video size in a movie](/documentation/quicktime-file-format/maximum_video_size_in_a_movie)
- [Maximum video size in a track](/documentation/quicktime-file-format/maximum_video_size_in_a_track)
- [Maximum video frame rate in a single track](/documentation/quicktime-file-format/maximum_video_frame_rate_in_a_single_track)
- [Average video frame rate in a single track](/documentation/quicktime-file-format/average_video_frame_rate_in_a_single_track)
- [Video variable frame rate indication](/documentation/quicktime-file-format/video_variable_frame_rate_indication)
- [Audio sample rate for a sample entry](/documentation/quicktime-file-format/audio_sample_rate_for_a_sample_entry)
- [Audio variable bit rate indication](/documentation/quicktime-file-format/audio_variable_bit_rate_indication)
- [Audio channel count](/documentation/quicktime-file-format/audio_channel_count)

### Media data atom types

- [Sprite media](/documentation/quicktime-file-format/sprite_media)
- [Sprite track properties](/documentation/quicktime-file-format/sprite_track_properties)
- [Sprite track media format](/documentation/quicktime-file-format/sprite_track_media_format)
- [Sprite media atom and data types](/documentation/quicktime-file-format/sprite_media_atom_and_data_types)
- [Sprite button behaviors](/documentation/quicktime-file-format/sprite_button_behaviors)
- [QT atom container description key](/documentation/quicktime-file-format/qt_atom_container_description_key)
- [Sprite media handler track properties QT atom container format](/documentation/quicktime-file-format/sprite_media_handler_track_properties_qt_atom_container_format)
- [Sprite media handler sample QT atom container formats](/documentation/quicktime-file-format/sprite_media_handler_sample_qt_atom_container_formats)
- [Wired action grammar](/documentation/quicktime-file-format/wired_action_grammar)
- [Tween media](/documentation/quicktime-file-format/tween_media)

#### Storing tween media

- [Tween sample description](/documentation/quicktime-file-format/tween_sample_description)
- [Tween sample data](/documentation/quicktime-file-format/tween_sample_data)
- [Tween type categories](/documentation/quicktime-file-format/tween_type_categories)
- [Tween QT atom container](/documentation/quicktime-file-format/tween_qt_atom_container)

##### General tween atoms

- [kTweenEntry](/documentation/quicktime-file-format/ktweenentry)
- [kTweenStartOffset](/documentation/quicktime-file-format/ktweenstartoffset)
- [kTweenDuration](/documentation/quicktime-file-format/ktweenduration)
- [kTweenData](/documentation/quicktime-file-format/ktweendata)
- [kNameAtom](/documentation/quicktime-file-format/knameatom)
- [kTweenType](/documentation/quicktime-file-format/ktweentype)

##### Path Tween Atoms

- [kTweenFlags](/documentation/quicktime-file-format/ktweenflags)
- [kInitialRotationAtom](/documentation/quicktime-file-format/kinitialrotationatom)

##### List Tween Atoms

- [kListElementType](/documentation/quicktime-file-format/klistelementtype)

##### 3D Tween Atoms

- [kTween3dInitialCondition](/documentation/quicktime-file-format/ktween3dinitialcondition)

##### Interpolation Tween Atoms

- [kTweenOutputMax](/documentation/quicktime-file-format/ktweenoutputmax)
- [kTweenOutputMin](/documentation/quicktime-file-format/ktweenoutputmin)
- [kTweenInterpolationID](/documentation/quicktime-file-format/ktweeninterpolationid)

##### Region Tween Atoms

- [kTweenPictureData](/documentation/quicktime-file-format/ktweenpicturedata)
- [kTweenRegionData](/documentation/quicktime-file-format/ktweenregiondata)
- [kTweenSequenceElement](/documentation/quicktime-file-format/ktweensequenceelement)
- [3D media](/documentation/quicktime-file-format/3d_media)
- [VR media](/documentation/quicktime-file-format/vr_media)

#### Describing VR worlds

- [QTVR string atom](/documentation/quicktime-file-format/qtvr_string_atom)

##### Data fields

- [stringUsage](/documentation/quicktime-file-format/qtvr_string_atom/stringusage)
- [stringLength](/documentation/quicktime-file-format/qtvr_string_atom/stringlength)
- [theString](/documentation/quicktime-file-format/qtvr_string_atom/thestring)
- [VR world atom container](/documentation/quicktime-file-format/vr_world_atom_container)
- [VR world header atom](/documentation/quicktime-file-format/vr_world_header_atom)

##### Data fields

- [majorVersion](/documentation/quicktime-file-format/vr_world_header_atom/majorversion)
- [minorVersion](/documentation/quicktime-file-format/vr_world_header_atom/minorversion)
- [nameAtomID](/documentation/quicktime-file-format/vr_world_header_atom/nameatomid)
- [defaultNodeID](/documentation/quicktime-file-format/vr_world_header_atom/defaultnodeid)
- [vrWorldFlags](/documentation/quicktime-file-format/vr_world_header_atom/vrworldflags)
- [reserved1](/documentation/quicktime-file-format/vr_world_header_atom/reserved1)
- [reserved2](/documentation/quicktime-file-format/vr_world_header_atom/reserved2)
- [Imaging parent atom](/documentation/quicktime-file-format/imaging_parent_atom)
- [Panorama imaging atom](/documentation/quicktime-file-format/panorama_imaging_atom)

##### Data fields

- [majorVersion](/documentation/quicktime-file-format/panorama_imaging_atom/majorversion)
- [minorVersion](/documentation/quicktime-file-format/panorama_imaging_atom/minorversion)
- [imagingMode](/documentation/quicktime-file-format/panorama_imaging_atom/imagingmode)
- [imagingValidFlags](/documentation/quicktime-file-format/panorama_imaging_atom/imagingvalidflags)
- [correction](/documentation/quicktime-file-format/panorama_imaging_atom/correction)
- [quality](/documentation/quicktime-file-format/panorama_imaging_atom/quality)
- [directDraw](/documentation/quicktime-file-format/panorama_imaging_atom/directdraw)
- [imagingProperties](/documentation/quicktime-file-format/panorama_imaging_atom/imagingproperties)
- [reserved1](/documentation/quicktime-file-format/panorama_imaging_atom/reserved1)
- [reserved2](/documentation/quicktime-file-format/panorama_imaging_atom/reserved2)
- [Node parent atom](/documentation/quicktime-file-format/node_parent_atom)
- [Node location atom structure ('nloc')](/documentation/quicktime-file-format/node_location_atom_structure)

#### Data fields

- [majorVersion](/documentation/quicktime-file-format/node_location_atom_structure/majorversion)
- [minorVersion](/documentation/quicktime-file-format/node_location_atom_structure/minorversion)
- [nodeType](/documentation/quicktime-file-format/node_location_atom_structure/nodetype)
- [locationFlags](/documentation/quicktime-file-format/node_location_atom_structure/locationflags)
- [locationData](/documentation/quicktime-file-format/node_location_atom_structure/locationdata)
- [reserved1](/documentation/quicktime-file-format/node_location_atom_structure/reserved1)
- [reserved2](/documentation/quicktime-file-format/node_location_atom_structure/reserved2)
- [Custom cursor atom](/documentation/quicktime-file-format/custom_cursor_atom)
- [Node information atom container](/documentation/quicktime-file-format/node_information_atom_container)

#### Specifying node information

- [Node header atom ('ndhd')](/documentation/quicktime-file-format/node_header_atom)

##### Data fields

- [majorVersion](/documentation/quicktime-file-format/node_header_atom/majorversion)
- [minorVersion](/documentation/quicktime-file-format/node_header_atom/minorversion)
- [nodeType](/documentation/quicktime-file-format/node_header_atom/nodetype)
- [nodeID](/documentation/quicktime-file-format/node_header_atom/nodeid)
- [nameAtomID](/documentation/quicktime-file-format/node_header_atom/nameatomid)
- [commentAtomID](/documentation/quicktime-file-format/node_header_atom/commentatomid)
- [reserved1](/documentation/quicktime-file-format/node_header_atom/reserved1)
- [reserved2](/documentation/quicktime-file-format/node_header_atom/reserved2)
- [Hot spot parent atom ('hspa')](/documentation/quicktime-file-format/hot_spot_parent_atom)
- [Hot spot information atom ('hsin')](/documentation/quicktime-file-format/hot_spot_information_atom)

##### Data fields

- [majorVersion](/documentation/quicktime-file-format/hot_spot_information_atom/majorversion)
- [minorVersion](/documentation/quicktime-file-format/hot_spot_information_atom/minorversion)
- [hotSpotType](/documentation/quicktime-file-format/hot_spot_information_atom/hotspottype)
- [nameAtomID](/documentation/quicktime-file-format/hot_spot_information_atom/nameatomid)
- [commentAtomID](/documentation/quicktime-file-format/hot_spot_information_atom/commentatomid)
- [cursorID](/documentation/quicktime-file-format/hot_spot_information_atom/cursorid)
- [bestPan](/documentation/quicktime-file-format/hot_spot_information_atom/bestpan)
- [bestTilt](/documentation/quicktime-file-format/hot_spot_information_atom/besttilt)
- [bestFOV](/documentation/quicktime-file-format/hot_spot_information_atom/bestfov)
- [bestViewCenter](/documentation/quicktime-file-format/hot_spot_information_atom/bestviewcenter)
- [hotSpotRect](/documentation/quicktime-file-format/hot_spot_information_atom/hotspotrect)
- [flags](/documentation/quicktime-file-format/hot_spot_information_atom/flags)
- [reserved1](/documentation/quicktime-file-format/hot_spot_information_atom/reserved1)
- [reserved2](/documentation/quicktime-file-format/hot_spot_information_atom/reserved2)
- [Specific information atom](/documentation/quicktime-file-format/specific_information_atom)
- [Link hot spot atom ('link')](/documentation/quicktime-file-format/link_hot_spot_atom)

##### Data fields

- [majorVersion](/documentation/quicktime-file-format/link_hot_spot_atom/majorversion)
- [minorVersion](/documentation/quicktime-file-format/link_hot_spot_atom/minorversion)
- [toNodeID](/documentation/quicktime-file-format/link_hot_spot_atom/tonodeid)
- [fromValidFlags](/documentation/quicktime-file-format/link_hot_spot_atom/fromvalidflags)
- [fromPan](/documentation/quicktime-file-format/link_hot_spot_atom/frompan)
- [fromTilt](/documentation/quicktime-file-format/link_hot_spot_atom/fromtilt)
- [fromFOV](/documentation/quicktime-file-format/link_hot_spot_atom/fromfov)
- [fromViewCenter](/documentation/quicktime-file-format/link_hot_spot_atom/fromviewcenter)
- [toValidFlags](/documentation/quicktime-file-format/link_hot_spot_atom/tovalidflags)
- [toPan](/documentation/quicktime-file-format/link_hot_spot_atom/topan)
- [toTilt](/documentation/quicktime-file-format/link_hot_spot_atom/totilt)
- [toFOV](/documentation/quicktime-file-format/link_hot_spot_atom/tofov)
- [toViewCenter](/documentation/quicktime-file-format/link_hot_spot_atom/toviewcenter)
- [distance](/documentation/quicktime-file-format/link_hot_spot_atom/distance)
- [flags](/documentation/quicktime-file-format/link_hot_spot_atom/flags)
- [reserved1](/documentation/quicktime-file-format/link_hot_spot_atom/reserved1)
- [reserved2](/documentation/quicktime-file-format/link_hot_spot_atom/reserved2)
- [URL hot spot atom](/documentation/quicktime-file-format/url_hot_spot_atom)
- [Support for wired actions](/documentation/quicktime-file-format/support_for_wired_actions)
- [QuickTime VR file format](/documentation/quicktime-file-format/quicktime_vr_file_format)

#### Storing QuickTime VR files

- [Single-node panoramic movies](/documentation/quicktime-file-format/single-node_panoramic_movies)
- [Single-node object movies](/documentation/quicktime-file-format/single-node_object_movies)
- [Multinode movies](/documentation/quicktime-file-format/multinode_movies)
- [Getting the name of a QuickTime VR node](/documentation/quicktime-file-format/getting_the_name_of_a_quicktime_vr_node)
- [Adding custom atoms in a QuickTime VR movie](/documentation/quicktime-file-format/adding_custom_atoms_in_a_quicktime_vr_movie)
- [Adding atom containers in a QuickTime VR Movie](/documentation/quicktime-file-format/adding_atom_containers_in_a_quicktime_vr_movie)
- [Optimizing QuickTime VR movies for web playback](/documentation/quicktime-file-format/optimizing_quicktime_vr_movies_for_web_playback)

##### Optimizations

- [The QTVR flattener](/documentation/quicktime-file-format/the_qtvr_flattener)
- [Sample atom container for the QTVR flattener](/documentation/quicktime-file-format/sample_atom_container_for_the_qtvr_flattener)
- [QTVR track](/documentation/quicktime-file-format/qtvr_track)

#### Storing sample descriptions

- [QuickTime VR sample description ('qtvr')](/documentation/quicktime-file-format/quicktime_vr_sample_description)

##### Data fields

- [size](/documentation/quicktime-file-format/quicktime_vr_sample_description/size)
- [type](/documentation/quicktime-file-format/quicktime_vr_sample_description/type)
- [reserved1](/documentation/quicktime-file-format/quicktime_vr_sample_description/reserved1)
- [reserved2](/documentation/quicktime-file-format/quicktime_vr_sample_description/reserved2)
- [dataRefIndex](/documentation/quicktime-file-format/quicktime_vr_sample_description/datarefindex)
- [data](/documentation/quicktime-file-format/quicktime_vr_sample_description/data)
- [Panorama tracks](/documentation/quicktime-file-format/panorama_tracks)

#### Storing panorama tracks

- [Panorama sample atom ('pdat')](/documentation/quicktime-file-format/panorama_sample_atom)

##### Data fields

- [majorVersion](/documentation/quicktime-file-format/panorama_sample_atom/majorversion)
- [minorVersion](/documentation/quicktime-file-format/panorama_sample_atom/minorversion)
- [imageRefTrackIndex](/documentation/quicktime-file-format/panorama_sample_atom/imagereftrackindex)
- [hotSpotRefTrackIndex](/documentation/quicktime-file-format/panorama_sample_atom/hotspotreftrackindex)
- [minPan](/documentation/quicktime-file-format/panorama_sample_atom/minpan)
- [maxPan](/documentation/quicktime-file-format/panorama_sample_atom/maxpan)
- [minTilt](/documentation/quicktime-file-format/panorama_sample_atom/mintilt)
- [maxTilt](/documentation/quicktime-file-format/panorama_sample_atom/maxtilt)
- [minFieldOfView](/documentation/quicktime-file-format/panorama_sample_atom/minfieldofview)
- [maxFieldOfView](/documentation/quicktime-file-format/panorama_sample_atom/maxfieldofview)
- [defaultPan](/documentation/quicktime-file-format/panorama_sample_atom/defaultpan)
- [defaultTilt](/documentation/quicktime-file-format/panorama_sample_atom/defaulttilt)
- [defaultFieldOfView](/documentation/quicktime-file-format/panorama_sample_atom/defaultfieldofview)
- [imageSizeX](/documentation/quicktime-file-format/panorama_sample_atom/imagesizex)
- [imageSizeY](/documentation/quicktime-file-format/panorama_sample_atom/imagesizey)
- [imageNumFramesX](/documentation/quicktime-file-format/panorama_sample_atom/imagenumframesx)
- [imageNumFramesY](/documentation/quicktime-file-format/panorama_sample_atom/imagenumframesy)
- [hotSpotSizeX](/documentation/quicktime-file-format/panorama_sample_atom/hotspotsizex)
- [hotSpotSizeY](/documentation/quicktime-file-format/panorama_sample_atom/hotspotsizey)
- [hotSpotNumFramesX](/documentation/quicktime-file-format/panorama_sample_atom/hotspotnumframesx)
- [hotSpotNumFramesY](/documentation/quicktime-file-format/panorama_sample_atom/hotspotnumframesy)
- [flags](/documentation/quicktime-file-format/panorama_sample_atom/flags)
- [panoType](/documentation/quicktime-file-format/panorama_sample_atom/panotype)
- [reserved2](/documentation/quicktime-file-format/panorama_sample_atom/reserved2)
- [Panorama image track](/documentation/quicktime-file-format/panorama_image_track)
- [Cylindrical panoramas](/documentation/quicktime-file-format/cylindrical_panoramas)
- [Cubic panoramas](/documentation/quicktime-file-format/cubic_panoramas)

#### Storing cubic image nodes

- [Image tracks in cubic nodes](/documentation/quicktime-file-format/image_tracks_in_cubic_nodes)
- [Panorama tracks in cubic nodes](/documentation/quicktime-file-format/panorama_tracks_in_cubic_nodes)
- [Nonstandard cubes](/documentation/quicktime-file-format/nonstandard_cubes)
- [Hot spot image tracks](/documentation/quicktime-file-format/hot_spot_image_tracks)

#### Hot spot image tracks

- [Low-resolution image tracks](/documentation/quicktime-file-format/low-resolution_image_tracks)
- [Track reference entry structure](/documentation/quicktime-file-format/track_reference_entry_structure)
- [Object tracks](/documentation/quicktime-file-format/object_tracks)

#### Storing object tracks

- [Object sample atom](/documentation/quicktime-file-format/object_sample_atom)

##### Data fields

- [majorVersion](/documentation/quicktime-file-format/object_sample_atom/majorversion)
- [minorVersion](/documentation/quicktime-file-format/object_sample_atom/minorversion)
- [movieType](/documentation/quicktime-file-format/object_sample_atom/movietype)
- [viewStateCount](/documentation/quicktime-file-format/object_sample_atom/viewstatecount)
- [defaultViewState](/documentation/quicktime-file-format/object_sample_atom/defaultviewstate)
- [mouseDownViewState](/documentation/quicktime-file-format/object_sample_atom/mousedownviewstate)
- [viewDuration](/documentation/quicktime-file-format/object_sample_atom/viewduration)
- [columns](/documentation/quicktime-file-format/object_sample_atom/columns)
- [rows](/documentation/quicktime-file-format/object_sample_atom/rows)
- [mouseMotionScale](/documentation/quicktime-file-format/object_sample_atom/mousemotionscale)
- [minPan](/documentation/quicktime-file-format/object_sample_atom/minpan)
- [maxPan](/documentation/quicktime-file-format/object_sample_atom/maxpan)
- [defaultPan](/documentation/quicktime-file-format/object_sample_atom/defaultpan)
- [minTilt](/documentation/quicktime-file-format/object_sample_atom/mintilt)
- [maxTilt](/documentation/quicktime-file-format/object_sample_atom/maxtilt)
- [defaultTilt](/documentation/quicktime-file-format/object_sample_atom/defaulttilt)
- [minFieldOfView](/documentation/quicktime-file-format/object_sample_atom/minfieldofview)
- [fieldOfView](/documentation/quicktime-file-format/object_sample_atom/fieldofview)
- [defaultFieldOfView](/documentation/quicktime-file-format/object_sample_atom/defaultfieldofview)
- [defaultViewCenterH](/documentation/quicktime-file-format/object_sample_atom/defaultviewcenterh)
- [defaultViewCenterV](/documentation/quicktime-file-format/object_sample_atom/defaultviewcenterv)
- [viewRate](/documentation/quicktime-file-format/object_sample_atom/viewrate)
- [frameRate](/documentation/quicktime-file-format/object_sample_atom/framerate)
- [animationSettings](/documentation/quicktime-file-format/object_sample_atom/animationsettings)
- [controlSettings](/documentation/quicktime-file-format/object_sample_atom/controlsettings)
- [Track references for object tracks](/documentation/quicktime-file-format/track_references_for_object_tracks)
- [QuickTime image file format](/documentation/quicktime-file-format/appendix_a_quicktime_image_file_format)

#### Storing image data

- [Atom types in QuickTime image files](/documentation/quicktime-file-format/atom_types_in_quicktime_image_files)
- [Recommended file type and suffix](/documentation/quicktime-file-format/recommended_file_type_and_suffix)
- [Summary of VR World and node atom types](/documentation/quicktime-file-format/appendix_e_summary_of_vr_world_and_node_atom_types)

#### C Summary

- [Constants](/documentation/quicktime-file-format/constants)
- [Data types](/documentation/quicktime-file-format/data_types)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
