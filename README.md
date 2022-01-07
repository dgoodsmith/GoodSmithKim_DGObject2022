# GoodSmithKim_DGObject2022
Data for "Flexible encoding of objects and space in single cells of the dentate gyrus"



Folders:

* Firing properties contains basic firing properties of cells analyzed here. Data is furhter divided between all 366 putative excitatory cells analyzed and active cells (cells with at least one place field in at least one session. This contains all individual firing rate maps for all sessions (used throughout but particularly in Figures 5 and S3), as well as data presented in Figure 2.

* RF_classificaiton contains training data and classificaiton features for the random forests classifier used to separate between mossy cells and granule cells. This data is presented in Figures 2 and S2

* Two_env folder contains data presented in figures 7 and S4, results of recordings in two environments containing the same objects

Files:

* session_info contains the following:
  * session_id: session type for each session. 0) No object (not analyzed in present study) 1) STD, 2) ADD, 3) MOVE
  * For object_locs and object_loc_px: object locations for each session. Each row is one object, and columns are x and y coordinates.
    * object_locs: Object locations in camera xcoordinates (480x640)
    * object_loc_px: object locations in pixels (48x64)
  * man_obj: manipulated object. Number corresponds to row in object_locs that represents the new (in ADD) or moved (in MOVE) sessions
  * active_sessions_info contains same information for 188 active cells (cells with at least one place field detected in at least one session). 
  
* FR_near_away_obj, data used for Figure 3C:
  * active_cl: classification for 188 active cells (cells with at least one place field), 0 = mossy cell, 1 = granule cell
  * obj_mean: mean firing within 10 pixels of object locations
  * non_obj_mean: mean firing rate >10 pixels from all object
  * away_median: median value of non_obj_mean used for statistical comparisons
  * near_median: median value of obj_mean used for statistical comparisons 

* landmark_vector, data used for Figures 4 and S3. Contains the following:
  * min_diff: minimum vector difference from place field to object for each session. Sessions where vector differences could not be calcuated (<2 fields) are given NaN values.
    * min_diff_gc and min_diff_mc are minimum vector differences separated by cell type
    * min_diff_active: same but only including cells with at least one field
  * PF_centers: x/y coordinates of place field centroids for all place fields.
  * GC_shuffle_LVs: number of detected LV responses in each of 100 shuffles of granule cell data (p value is number >= observed 13 responses)
  * MC_shuffle_LVs: number of detected LV responses in each of 100 shuffles of mossy cell data (p value is number>= observed 50 responses)

* distance_to_fields, data used for Figure 6A:
  * for all 286 pairs of consecutive STD and MAN sessions (excluding pairs with no place fields in either session):
    * session_pair_rmaps: rate maps for STD (column 1) and MAN (column 2)
    * session_pair_cl: classification for each cell, 0 = mossy cell, 1 = granule cell
    * min_dist: distance from manipulated object location to nearest place field center (column 1 is STD session, column 2 is MAN session)
    * min_unman_dist: same but for unmanipulated object
    * min_dist_diff: difference between minimum distance in MAN and STD sessions for manipulated object
    * min_unman_dist_diff: same but for unmanipulated object. 
 
* STD_MAN_STD_correlation, data used for Figure 6C:
  * sess_group_map: rate maps for groups of consecutive STD, MAN, STD sessions with place fields that were analyzed in Figure 6C
  * sess_group_cl: cell type classification for rate maps in sess_group_map, 0 = mossy cell, 1 = granule cell
  * gcl_std: Rstd (correlation between two STD rate maps) for granule cells.
  * gcl_man: Rman (correlation between STD and MAN rate maps) for granule cells
  * gcl_diff: difference between Rstd and Rman for granule cells
  * mc_std: Rstd for mossy cells
  * mc_man: Rman for mossy cells
  * mc_diff: difference between Rstd and Rman for mossy cells
  * gc_shuffle_diff: distribution of differences between Rstd and Rman for shuffled granule cell data
  * mossy_shuffle_diff: distribution of differences between Rstd and Rman for shuffled mossy cell data

* local_rmap, data used for Figure 6E:
  * gc_object, mc_object: correlation value for "object-related" local rate map areas
  * gc_spatial, mc_spatial: correlation value for spatial" local rate map areas
  * gc_diff, mc_diff: difference between object-related and spatial local rate map correlations 
  * gc_unman_object, mc_unman_object, gc_unman_spatial, mc_unman_spatial, gc_unman_diff, mc_unman_diff: same as above but for local rate maps centered at unmoved object location
  * For all above: nan values indicate insufficient activity in one or both local rmap areas for correlation
  * man_obj_loc: location of moved object in MAN session
  * unman_obj_loc: location of unmoved object
  * session_pair_cl: cell type classification for session pairs used for local rmap analysis
  * session_pair_maps: rate maps for STD/MAN session pairs used for local rmap analysis
  * session_pair_object: object locations for STD/MAN session pairs used for local rmap analysis

