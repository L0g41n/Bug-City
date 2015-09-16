----------------------------------------------------
1. Order matters.
2. If there can be multiple of something, repeat the name on a new line.
----------------------------------------------------

Example (*.ambi.txt) ambience template file:

/** This is the name of the ambience template */
id: "barrens"
ambience {
	/** Name of the sound clip to play. (technically optional but required if there is sound to play) */
	sound_clip: "BarrensExt"
	
	/** Volume of the sound, default is 1.0. (optional) */
	volume: 1.0
	
	/** Start time from the start of clip, if more than one then randomly choose a start time. (optional) (multiple) */
	start_time: 0.0
	start_time: 0.1
	
	/** Pitch of the sound, default is 1.0. (optional) */
	pitch: 1.2
	
	/** If set, use random pitch from random_pitch to pitch. (optional) */
	random_pitch: 0.8
	
	/** Frequency weight that the ambience should play with ambience of the same layer, from 0.0 to 1.0, default is 0.5. (optional) */
	frequency: 1.0
	
	/** Delay in seconds of when the ambience should play. (optional) */
	delay: 3.0
	
	/** If set more than 0.0, use random delay from random_delay to delay. (optional) */
	random_delay: 0.1
	
	/** Manual set of ambience length in seconds, otherwise use sound clip length. Better to leave unused unless necessary. (optional) */
	length: 3.2
	
	/** If looping, default to false. (optional) */
	looping: true
	
	/** This is used to put different ambience into a set that should be chosen inclusively using frequency. Layer from 0 to 3. (required) */
	layer: 0
}
ambience {
	sound_clip: "Car"
	volume: 1.0
	frequency: 0.5
	delay: 10.0
	random_delay: 8.0
	layer: 1
}
ambience {
	sound_clip: "CreatureB"
	volume: 0.5
	frequency: 0.125
	delay: 10.0
	random_delay: 8.0
	layer: 1
}
ambience {
	sound_clip: "Gun"
	volume: 1.0
	frequency: 0.25
	delay: 3.0
	random_delay: 1.0
	layer: 1
}
ambience {
	sound_clip: "CreatureD"
	volume: 0.5
	frequency: 0.125
	delay: 8.0
	random_delay: 6.0
	layer: 1
}
ambience {
	sound_clip: "CarHorn"
	volume: 1.0
	frequency: 0.25
	delay: 3.0
	random_delay: 1.0
	layer: 2
}
ambience {
	sound_clip: "CarAlarm"
	volume: 1.0
	frequency: 0.125
	delay: 12.0
	random_delay: 10.0
	layer: 2
}
ambience {
	sound_clip: "Siren"
	volume: 1.0
	frequency: 0.125
	delay: 18.0
	random_delay: 14.0
	layer: 2
}
ambience {
	sound_clip: "Trash"
	volume: 1.0
	frequency: 0.5
	delay: 8.0
	random_delay: 6.0
	layer: 2
}

/** Necessary to add what audio bundles are being used which are the folder names that the sounds are in. (required) (multiple) */
audio_bundles: "hongkong:ambient_barrens"