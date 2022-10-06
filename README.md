# pintrix_matrices

Repository for keeping matrix definition files for pinball machines - currently used in the app pintrix available on the iOS and Google Play stores

* [Apple App Store](https://apps.apple.com/us/app/pintrix/id1017596411)
* [Google Play Store](https://play.google.com/store/apps/details?id=com.chunkout.pintrix&hl=en&gl=US)

## File format
```yaml
gameMatrices:
    Lamp: # Lamp matrix defintion
        columns:
            '1': # The Column ID - repeat this group for each column
                connectorID: CN7 # The name of the connector this column is attached to
                connectorPin: 1  # The number of the pin this column is attached to
                icNumber: Q71    # The identifier of the IC / Transistor this column is attached to
                icPin: '-'       # The pin on the IC this column is attached to
                wireColour: Yellow-Brown # The colour of the wiring for this column - primary colour first, stripe second
            # Repeat above column definition for all columns (typically 8)
            
        matrixItems:
            1: # The ID for this specific matrix item (usually the number in the box in the manual - e.g. 23. Some manufacturers used the row/column numbers, some were sequential)
                columnIdentifier: '1'     # Column identifier from the columns array above
                itemName: 10 Yard Bottom  # Name of the matrix item
                normallyClosedFlag: 0     # Whether the item is declared normally open (only used for switches really)
                rowIdentifier: '1'        # Row identifier from the rows array below
                usedFlag: 1               # Whether this matrix item is used or not (0 = not used)
            # Repeat above matrixItem definition for all matrix items (typically 64)
            
        rows:
            '1': # The Row ID - repeat this group for each row
                connectorID: CN6 # The name of the connector this row is attached to
                connectorPin: 1  # The number of the pin this row is attached to
                icNumber: Q72    # The identifier of the IC / Transistor this row is attached to
                icPin: '-'       # The pin on the IC this row is attached to
                wireColour: Red-Brown # The colour of the wiring for this row - primary colour first, stripe second
            # Repeat above row definition for all rows (typically 8)
            
    Switch: # Switch matrix defintion
        columns:
            '1': # The Column ID - repeat this group for each column
                connectorID: CN8 # The name of the connector this column is attached to
                connectorPin: 1  # The number of the pin this column is attached to
                icNumber: Q55    # The identifier of the IC / Transistor this column is attached to
                icPin: '-'       # The pin on the IC this column is attached to
                wireColour: Green-Brown # The colour of the wiring for this column - primary colour first, stripe second
            # Repeat above column definition for all columns (typically 8)
            
        matrixItems:
            1: # The ID for this specific matrix item (usually the number in the box in the manual - e.g. 23. Some manufacturers used the row/column numbers, some were sequential)
                columnIdentifier: '1'     # Column identifier from the columns array above
                itemName: PLUMB TILT  # Name of the matrix item
                normallyClosedFlag: 0     # Whether the item is declared normally open (only used for switches really)
                rowIdentifier: '1'        # Row identifier from the rows array below
                usedFlag: 1               # Whether this matrix item is used or not (0 = not used)
            # Repeat above matrixItem definition for all matrix items (typically 64)
            
        rows:
            '1': # The Row ID - repeat this group for each row
                connectorID: CN10 # The name of the connector this row is attached to
                connectorPin: 9  # The number of the pin this row is attached to
                icNumber: '-'    # The identifier of the IC / Transistor this row is attached to
                icPin: '-'       # The pin on the IC this row is attached to
                wireColour: White-Brown # The colour of the wiring for this row - primary colour first, stripe second
            # Repeat above row definition for all rows (typically 8)
            
gameName: Monday Night Football # Name of the game
isReady: 1                      # Is this ready to use in app
manufacturerName: Data East     # Name of manufacturer
releaseMonth: 9                 # Month game was released
releaseYear: 1989               # Year game was released
```
