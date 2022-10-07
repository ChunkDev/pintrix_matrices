# pintrix_matrices

Repository for keeping matrix definition files for pinball machines - currently used in the app pintrix available on the iOS and Google Play stores

* [Apple App Store](https://apps.apple.com/us/app/pintrix/id1017596411)
* [Google Play Store](https://play.google.com/store/apps/details?id=com.chunkout.pintrix&hl=en&gl=US)

## File format
```yaml
gameName: Monday Night Football
isReady: 1
manufacturerName: Data East
releaseYear: 1989
releaseMonth: 9
ipdbLink: ''  # Link to the Internet Pinball Database website
opdbId: ''    # Identifier for the Open Pinball Database - see https://opdb.org/about
gameMatrices:
    lamp: # Lamp matrix defintion
        columns:
            '1': # The Column ID - repeat this group for each column
                connectorID: CN7 # The name of the connector this column is attached to
                connectorPin: 1  # The number of the pin this column is attached to
                icNumber: Q71    # The identifier of the IC / Transistor this column is attached to
                icPin: '-'       # The pin on the IC this column is attached to
                wireColour: Yellow-Brown # The colour of the wiring for this column - primary colour first, stripe second
            # Repeat above column definition for all columns (typically 8)
        rows:
            '1': # The Row ID - repeat this group for each row
                connectorID: CN6 # The name of the connector this row is attached to
                connectorPin: 1  # The number of the pin this row is attached to
                icNumber: Q72    # The identifier of the IC / Transistor this row is attached to
                icPin: '-'       # The pin on the IC this row is attached to
                wireColour: Red-Brown # The colour of the wiring for this row - primary colour first, stripe second
            # Repeat above row definition for all rows (typically 8)
        matrixElements:
            1: # The ID for this specific matrix element (usually the number in the box in the manual - e.g. 23. Some manufacturers used the row/column numbers, some were sequential)
                column: '1'           # Column identifier from the columns array above
                row: '1'              # Row identifier from the rows array below
                name: 10 Yard Bottom  # Name of the matrix element
                normallyClosedFlag: 0 # Whether the element is declared normally open (only used for switches really)
                
                usedFlag: 1               # Whether this matrix element is used or not (0 = not used)
            # Repeat above matrixElement definition for all matrix elements (typically 64)
            
    switch: # Switch matrix defintion
        columns:
            '1': # The Column ID - repeat this group for each column
                connectorID: CN8 # The name of the connector this column is attached to
                connectorPin: 1  # The number of the pin this column is attached to
                icNumber: Q55    # The identifier of the IC / Transistor this column is attached to
                icPin: '-'       # The pin on the IC this column is attached to
                wireColour: Green-Brown # The colour of the wiring for this column - primary colour first, stripe second
            # Repeat above column definition for all columns (typically 8)
        rows:
            '1': # The Row ID - repeat this group for each row
                connectorID: CN10 # The name of the connector this row is attached to
                connectorPin: 9  # The number of the pin this row is attached to
                icNumber: '-'    # The identifier of the IC / Transistor this row is attached to
                icPin: '-'       # The pin on the IC this row is attached to
                wireColour: White-Brown # The colour of the wiring for this row - primary colour first, stripe second
            # Repeat above row definition for all rows (typically 8)
        matrixElements:
            1: # The ID for this specific matrix element (usually the number in the box in the manual - e.g. 23. Some manufacturers used the row/column numbers, some were sequential)
                column: '1'           # Column identifier from the columns array above
                row: '1'              # Row identifier from the rows array below
                name: PLUMB TILT  # Name of the matrix element
                normallyClosedFlag: 0     # Whether the element is declared normally open (only used for switches really)
                usedFlag: 1               # Whether this matrix element is used or not (0 = not used)
            # Repeat above matrixElement definition for all matrix elements (typically 64)
```
