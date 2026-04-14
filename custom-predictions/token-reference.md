# Custom Predictions — Token Reference

Tokens are used in `match_tokens` to define the conditions under which a prediction is shown. Each token is a string in the format `"CATEGORY::TOKEN_NAME"`.

See [Introduction](/predictions/introduction) for how `match_tokens` conditions work.

---

## SELECTION

Tokens describing the state of the current selection.

| Token | Description |
| :--- | :--- |
| `SELECTION::ALL` | All elements are selected |
| `SELECTION::ANY` | At least one element is selected |
| `SELECTION::ISOLATED_TARGET` | The active element is isolated (nothing else selected) |
| `SELECTION::MULTIPLE` | More than one element is selected |
| `SELECTION::NONE` | Nothing is selected |
| `SELECTION::SINGLE` | Exactly one element is selected |
| `SELECTION::SUBSET` | Some but not all elements are selected |

---

## SCENE

Tokens describing the contents of the scene.

| Token | Description |
| :--- | :--- |
| `SCENE::HAS_ACTIVE_CAMERA` | The scene has an active camera |
| `SCENE::HAS_CAMERAS` | The scene contains at least one camera |
| `SCENE::HAS_HIGH_LOW_LODS` | The scene contains objects with `_high` / `_low` naming affixes |
| `SCENE::HAS_LIGHTS` | The scene contains at least one light |
| `SCENE::HAS_OBJECT_DIMENSIONS` | Objects in the scene have non-zero dimensions |
| `SCENE::HAS_OBJECT_MATERIALS` | Objects in the scene have materials assigned |
| `SCENE::HAS_OBJECT_VOLUMES` | Objects in the scene have non-zero volumes |
| `SCENE::HAS_SIMILAR_NAMES_TO_TARGET` | Other objects share a similar name to the active object |

---

## OBJECTS

Tokens describing object-level properties (Object Mode).

| Token | Description |
| :--- | :--- |
| `OBJECTS::HAS_MULTI_OBJECTS` | The view layer contains more than one object |
| `OBJECTS::HAS_SINGLE_OBJECT` | The view layer contains exactly one object |
| `OBJECTS::TARGET_HAS_DIMENSIONS` | The active object has non-zero dimensions |
| `OBJECTS::TARGET_HAS_HIGH_LOD_AFFIX` | The active object's name contains a `_high` affix |
| `OBJECTS::TARGET_HAS_LOW_LOD_AFFIX` | The active object's name contains a `_low` affix |
| `OBJECTS::TARGET_HAS_MATERIALS` | The active object has materials assigned |
| `OBJECTS::TARGET_HAS_MIRROR_AFFIX` | The active object's name contains an `L.` / `R.` mirror affix |
| `OBJECTS::TARGET_HAS_SHARED_DATA` | Other objects share the same object data as the active object |
| `OBJECTS::TARGET_HAS_VOLUME` | The active object has a non-zero volume |
| `OBJECTS::TARGET_IS_TYPE_ARMATURE` | The active object is an Armature |
| `OBJECTS::TARGET_IS_TYPE_CAMERA` | The active object is a Camera |
| `OBJECTS::TARGET_IS_TYPE_CURVE` | The active object is a Curve |
| `OBJECTS::TARGET_IS_TYPE_CURVES` | The active object is a Hair Curves object |
| `OBJECTS::TARGET_IS_TYPE_EMPTY` | The active object is an Empty |
| `OBJECTS::TARGET_IS_TYPE_FONT` | The active object is a Text object |
| `OBJECTS::TARGET_IS_TYPE_GREASEPENCIL` | The active object is a Grease Pencil object |
| `OBJECTS::TARGET_IS_TYPE_LATTICE` | The active object is a Lattice |
| `OBJECTS::TARGET_IS_TYPE_LIGHT` | The active object is a Light |
| `OBJECTS::TARGET_IS_TYPE_LIGHT_AREA` | The active object is an Area Light |
| `OBJECTS::TARGET_IS_TYPE_LIGHT_POINT` | The active object is a Point Light |
| `OBJECTS::TARGET_IS_TYPE_LIGHT_PROBE` | The active object is a Light Probe |
| `OBJECTS::TARGET_IS_TYPE_LIGHT_SPOT` | The active object is a Spot Light |
| `OBJECTS::TARGET_IS_TYPE_LIGHT_SUN` | The active object is a Sun Light |
| `OBJECTS::TARGET_IS_TYPE_MESH` | The active object is a Mesh |
| `OBJECTS::TARGET_IS_TYPE_META` | The active object is a Metaball |
| `OBJECTS::TARGET_IS_TYPE_POINTCLOUD` | The active object is a Point Cloud |
| `OBJECTS::TARGET_IS_TYPE_SPEAKER` | The active object is a Speaker |
| `OBJECTS::TARGET_IS_TYPE_SURFACE` | The active object is a Surface |
| `OBJECTS::TARGET_IS_TYPE_VOLUME` | The active object is a Volume |

---

## HIERARCHY

Tokens describing parent-child relationships of the active object (Object Mode).

| Token | Description |
| :--- | :--- |
| `HIERARCHY::TARGET_HAS_ANCESTORS` | The active object has one or more ancestors |
| `HIERARCHY::TARGET_HAS_CHILDREN` | The active object has direct children |
| `HIERARCHY::TARGET_HAS_DESCENDANTS` | The active object has descendants (children or deeper) |
| `HIERARCHY::TARGET_HAS_FAMILY` | The active object is part of a parent-child hierarchy |
| `HIERARCHY::TARGET_HAS_PARENT` | The active object has a direct parent |
| `HIERARCHY::TARGET_HAS_ROOT` | The active object has a root ancestor |
| `HIERARCHY::TARGET_HAS_SIBLINGS` | The active object has siblings (objects sharing the same parent) |
| `HIERARCHY::SELECTION_HAS_ANCESTORS` | At least one selected object has ancestors |
| `HIERARCHY::SELECTION_HAS_CHILDREN` | At least one selected object has children |
| `HIERARCHY::SELECTION_HAS_DESCENDANTS` | At least one selected object has descendants |
| `HIERARCHY::SELECTION_HAS_FAMILY` | At least one selected object is part of a hierarchy |
| `HIERARCHY::SELECTION_HAS_PARENT` | At least one selected object has a parent |
| `HIERARCHY::SELECTION_HAS_ROOT` | At least one selected object has a root ancestor |
| `HIERARCHY::SELECTION_HAS_SIBLINGS` | At least one selected object has siblings |

---

## MESH

Tokens describing the state of the active mesh (Edit Mesh Mode).

| Token | Description |
| :--- | :--- |
| `MESH::HAS_EDGE_BEVELS` | The mesh has edges with bevel weights |
| `MESH::HAS_EDGE_CREASES` | The mesh has edges with creases |
| `MESH::HAS_EDGE_SEAMS` | The mesh has edges marked as seams |
| `MESH::HAS_EDGE_SHARPS` | The mesh has edges marked as sharp |
| `MESH::HAS_INTERIOR_FACES` | The mesh has interior faces |
| `MESH::HAS_LOOSE_EDGES` | The mesh has loose edges |
| `MESH::HAS_LOOSE_FACES` | The mesh has loose faces |
| `MESH::HAS_LOOSE_VERTICES` | The mesh has loose vertices |
| `MESH::HAS_MULTI_EDGES` | The mesh has more than one edge |
| `MESH::HAS_MULTI_FACES` | The mesh has more than one face |
| `MESH::HAS_MULTI_VERTICES` | The mesh has more than one vertex |
| `MESH::HAS_NAKED_EDGES` | The mesh has naked (open boundary) edges |
| `MESH::HAS_NGONS` | The mesh has ngons (faces with more than 4 sides) |
| `MESH::HAS_QUADS` | The mesh has quads |
| `MESH::HAS_SELECTED_EDGES` | At least one edge is selected |
| `MESH::HAS_SELECTED_FACES` | At least one face is selected |
| `MESH::HAS_SELECTED_VERTICES` | At least one vertex is selected |
| `MESH::HAS_SINGLE_EDGE` | Exactly one edge is selected |
| `MESH::HAS_SINGLE_FACE` | Exactly one face is selected |
| `MESH::HAS_SINGLE_VERTEX` | Exactly one vertex is selected |
| `MESH::HAS_TRIANGLES` | The mesh has triangles |
| `MESH::IS_EDGE_MODE` | The mesh is in edge select mode |
| `MESH::IS_FACE_MODE` | The mesh is in face select mode |
| `MESH::IS_VERTEX_MODE` | The mesh is in vertex select mode |

---

## VERTICES

Tokens describing the active vertex or vertex selection (Edit Mesh Mode).

| Token | Description |
| :--- | :--- |
| `VERTICES::SELECTION_HAS_CONNECTED_VERTICES` | The selected vertices are connected to each other |
| `VERTICES::TARGET_HAS_MIRROR_X` | The active vertex has a mirror counterpart on the X axis |
| `VERTICES::TARGET_HAS_MIRROR_Y` | The active vertex has a mirror counterpart on the Y axis |
| `VERTICES::TARGET_HAS_MIRROR_Z` | The active vertex has a mirror counterpart on the Z axis |
| `VERTICES::TARGET_IN_VGROUP` | The active vertex belongs to a vertex group |

---

## EDGES

Tokens describing the active edge or edge selection (Edit Mesh Mode).

| Token | Description |
| :--- | :--- |
| `EDGES::SELECTION_HAS_CONNECTED_EDGES` | The selected edges form a connected chain |
| `EDGES::SELECTION_HAS_EDGE_CHAINS` | The selection contains edge chains |
| `EDGES::SELECTION_HAS_EDGE_LOOPS` | The selection contains edge loops |
| `EDGES::SELECTION_HAS_UNIFORM_LENGTHS` | The selected edges have uniform lengths |
| `EDGES::SELECTION_HAS_VARIED_LENGTHS` | The selected edges have varied lengths |
| `EDGES::SELECTION_IS_EDGE_CHAIN` | The entire selection forms a single edge chain |
| `EDGES::SELECTION_IS_EDGE_LOOP` | The entire selection forms a single edge loop |
| `EDGES::SELECTION_ONLY_EDGE_CHAINS` | The selection contains only edge chains |
| `EDGES::SELECTION_ONLY_EDGE_LOOPS` | The selection contains only edge loops |
| `EDGES::TARGET_HAS_BEVEL` | The active edge has a bevel weight |
| `EDGES::TARGET_HAS_CREASE` | The active edge has a crease |
| `EDGES::TARGET_HAS_MIRROR_X` | The active edge has a mirror counterpart on the X axis |
| `EDGES::TARGET_HAS_MIRROR_Y` | The active edge has a mirror counterpart on the Y axis |
| `EDGES::TARGET_HAS_MIRROR_Z` | The active edge has a mirror counterpart on the Z axis |
| `EDGES::TARGET_HAS_SEAM` | The active edge is marked as a seam |
| `EDGES::TARGET_HAS_SHARP` | The active edge is marked as sharp |
| `EDGES::TARGET_INSIDE_EDGE_RING` | The active edge is part of an edge ring |
| `EDGES::TARGET_IS_BOUNDARY_EDGE` | The active edge is a boundary edge |
| `EDGES::TARGET_IS_DANGLING_EDGE` | The active edge is a dangling edge |
| `EDGES::TARGET_IS_FACELESS_EDGE` | The active edge has no connected faces |
| `EDGES::TARGET_IS_FAUX_SHARP_EDGE` | The active edge is implicitly sharp due to face angle |
| `EDGES::TARGET_IS_MANIFOLD_EDGE` | The active edge is manifold (connected to exactly two faces) |
| `EDGES::TARGET_IS_NAKED_EDGE` | The active edge is naked (connected to only one face) |
| `EDGES::TARGET_IS_NON_MANIFOLD_EDGE` | The active edge is non-manifold |
| `EDGES::TARGET_IS_SHARED_EDGE` | The active edge is shared between faces |

---

## FACES

Tokens describing the active face or face selection (Edit Mesh Mode).

| Token | Description |
| :--- | :--- |
| `FACES::SELECTION_HAS_CONNECTED_FACES` | The selected faces are connected to each other |
| `FACES::SELECTION_HAS_FACE_ISLANDS` | The selection contains disconnected face islands |
| `FACES::TARGET_HAS_MIRROR_X` | The active face has a mirror counterpart on the X axis |
| `FACES::TARGET_HAS_MIRROR_Y` | The active face has a mirror counterpart on the Y axis |
| `FACES::TARGET_HAS_MIRROR_Z` | The active face has a mirror counterpart on the Z axis |
| `FACES::TARGET_IS_NGON` | The active face is an ngon |
| `FACES::TARGET_IS_QUAD` | The active face is a quad |
| `FACES::TARGET_IS_TRIANGLE` | The active face is a triangle |

---

## CURVES

Tokens describing the active curve (Edit Curve Mode).

| Token | Description |
| :--- | :--- |
| `CURVES::HAS_BEZIER_SPLINE` | The curve contains a Bezier spline |
| `CURVES::HAS_CONTROL_POINTS_SELECTED` | Control points are selected |
| `CURVES::HAS_HANDLES_SELECTED` | Bezier handles are selected |
| `CURVES::HAS_MULTI_POINTS` | The curve has more than one control point |
| `CURVES::HAS_NURBS_SPLINE` | The curve contains a NURBS spline |
| `CURVES::HAS_POINTS_SELECTED` | Any curve points are selected |
| `CURVES::HAS_POLY_SPLINE` | The curve contains a Poly spline |
| `CURVES::HAS_SINGLE_POINT` | Exactly one control point is selected |
| `CURVES::HAS_VARIED_DIRECTIONS` | The selected points have varied directions |
| `CURVES::HAS_VARIED_HANDLE_TYPES` | The selected Bezier handles have varied types |
| `CURVES::HAS_VARIED_RADII` | The selected points have varied radii |
| `CURVES::HAS_VARIED_SPLINE_TYPES` | The curve contains splines of different types |
| `CURVES::HAS_VARIED_TILTS` | The selected points have varied tilt values |
| `CURVES::HAS_VARIED_WEIGHTS` | The selected points have varied weights |

---

## BONES

Tokens describing bone state (Edit Armature and Pose Mode).

| Token | Description |
| :--- | :--- |
| `BONES::HAS_MIRROR` | The armature has a mirror bone counterpart |
| `BONES::HAS_MULTI_BONES` | The armature has more than one bone |
| `BONES::HAS_SINGLE_BONE` | Exactly one bone is selected |
| `BONES::SELECTION_HAS_SHARED_BONE_COLLECTIONS` | The selected bones share a bone collection |
| `BONES::SELECTION_HAS_SHARED_COLORS` | The selected bones share a color theme |
| `BONES::SELECTION_HAS_SHARED_LENGTHS` | The selected bones have similar lengths |
| `BONES::SELECTION_HAS_SHARED_PREFIXES` | The selected bones share a name prefix |
| `BONES::SELECTION_HAS_SHARED_SHAPES` | The selected bones share a custom shape |
| `BONES::SELECTION_HAS_SHARED_SUFFIXES` | The selected bones share a name suffix |
