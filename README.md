
# Rule-based RWP surface generation
Repository containing all resources used for the rule-based surface generation of Romanian Weak Pronouns (RWPs).

# Environment Configuration
- **File**: `jupyter_config.txt`

## RWP Input Formats
1. **`input_rwp_352.json`**: Contains notes, input, source, and targets.
2. **`rwp352_db.json`**: Contains notes, input, source, targets, patterns, and annotations for each sentence, including:
   - `schwa_dash_alternation`
   - `syllabic_dash_alternation`
   - `syntax`
   - `rwp_counter`
3. **`rwp352_lingeval_enriched_db.json`**:
   - Expanded annotations on patterns (for RWP-relevant sentences, i.e., only 346 sentences).
   - Includes notes, input, source, targets, patterns, and annotations.
4. **SpaCy-Annotated Input** (located in `spacyAnnotation` directory):
   - `rwp_352_corrected_annotation.json` (JSON format)
   - `rwp_352_corrected_annotation.spacy` (SpaCy binary format)

## Rule-Based Generation Task
- **Notebook**: `generate_rwp_surface_forms.ipynb`
- **Inputs**:
  1. `input_rwp_352.json`: Used to add the generation output.
  2. `spacyAnnotation/rwp_352_corrected_annotation.spacy`: For processing annotated data.
- **Outputs**:
  1. `logDir/logfile_82.log`: Debug logs.
  2. `genDir/genOpt_82.json`: Generated output.
     - **Note**: `'82'` is a version tag for comparing with previous outputs.

## Cleaning Notes and Source Subelements
- **Notebook**: `delete_subelements.ipynb`
- **Input**: `genDir/genOpt_82.json`
- **Output**: `clnDir/rule_based_oput_rwp352.json`

## Extract Features into CSV Format
- **Notebook**: `extract_attrs2csv.ipynb`
- **Input**: `rwp352_lingeval_enriched_db.json`
- **Output**: `db_features2csv/attrStats.csv`

