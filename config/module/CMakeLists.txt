# Compiles the in-repo caps_word_ext behavior into the ZMK app target so it
# sees ZMK's private headers. Only the central half runs behaviors.
if ((NOT CONFIG_ZMK_SPLIT) OR CONFIG_ZMK_SPLIT_ROLE_CENTRAL)
  target_sources_ifdef(CONFIG_ZMK_BEHAVIOR_CAPS_WORD_EXT app PRIVATE src/behavior_caps_word_ext.c)
endif()
