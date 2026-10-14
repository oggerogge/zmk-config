# Compiles the in-repo behaviors into the ZMK app target so they see
# ZMK's private headers. Only the central half runs behaviors.
if ((NOT CONFIG_ZMK_SPLIT) OR CONFIG_ZMK_SPLIT_ROLE_CENTRAL)
  target_sources_ifdef(CONFIG_ZMK_BEHAVIOR_CAPS_WORD_EXT app PRIVATE src/behavior_caps_word_ext.c)
  target_sources_ifdef(CONFIG_ZMK_BEHAVIOR_STICKY_KEY_EXT app PRIVATE src/behavior_sticky_key_ext.c)
endif()
