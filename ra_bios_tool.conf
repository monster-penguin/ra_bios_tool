# ==============================================================================
#  ra_bios_tool.conf - Configuration file for ra_bios_tool
# ==============================================================================
#
#  This file is sourced by ra_bios_script.sh at startup.
#  Edit the values below to match your system if the defaults are incorrect.
#
#  Lines beginning with # are comments and are ignored by the script.
#  Do not add quotes around values unless the path contains spaces.
#
# ==============================================================================


# ------------------------------------------------------------------------------
#  RETROARCH INSTALLATION PATHS
# ------------------------------------------------------------------------------

# Location of the RetroARCH core .info files.
# This is the directory the script scans to build the combined BIOS manifest.
# Default is the standard RetroARCH flatpak installation path.
RA_MANIFEST_SOURCE="/var/lib/flatpak/app/org.libretro.RetroArch/current/active/files/share/libretro/info/"

# Location of the live RetroARCH config directory on your system.
# This is the parent directory that contains system/, saves/, etc.
# This path is used during Step 11 (optional live population) and by the
# Step 13 cleanup safety check to prevent the staging folder from ever being
# mistaken for the live directory and deleted.
# Default is the standard RetroARCH flatpak user config directory.
RA_LIVE_DIR="$HOME/.var/app/org.libretro.RetroArch/config/retroarch"

# RetroARCH version this tool was built and tested against.
# This value is displayed in the version warning at startup.
RA_TESTED_VERSION="1.22.2"


# ------------------------------------------------------------------------------
#  RETROARCH INTERNAL FOLDER NAMES
# ------------------------------------------------------------------------------
#
#  RA_BIOS_FOLDER is the folder name used inside the retroarch/ staging
#  directory for all firmware and BIOS files. It corresponds to RetroARCH's
#  "system" directory.
#
#  All firmwareN_path values in RetroARCH .info files are relative to this
#  folder. For example, a .info entry with:
#    firmware0_path = "dc/dc_boot.bin"
#  will be placed at:
#    retroarch/system/dc/dc_boot.bin
#
#  Unlike RetroDECK, RetroARCH .info files do not reference saves/ or roms/
#  directories for firmware — all firmware paths are relative to system/ only.
#  Only change this if RetroARCH has renamed its system directory.

RA_BIOS_FOLDER="system"


# ------------------------------------------------------------------------------
#  TOOL OUTPUT PATHS
# ------------------------------------------------------------------------------

# These are all relative to the ra_bios_tool folder by default.
# You can set absolute paths here if you prefer outputs elsewhere.

# Location of the combined manifest JSON output
RA_MANIFEST_OUTPUT="$TOOL_DIR/combined_manifest.json"

# Location and filename of ra_bios_set.zip
RA_BIOS_ZIP="$TOOL_DIR/ra_bios_set.zip"

# Location of the retroarch/ staging output folder
RA_STAGING_DIR="$TOOL_DIR/retroarch"

# Directory where the CSV report is saved
RA_REPORT_DIR="$TOOL_DIR"

# Folder where files that failed MD5 hash checks are saved (Step 10, optional)
# These are files whose filename matched the manifest but whose hash did not.
RA_FAILED_HASH_DIR="$TOOL_DIR/failed_hash_checks"

# ==============================================================================
