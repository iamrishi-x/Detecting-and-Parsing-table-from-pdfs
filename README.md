# Techniques for detecting table 

1. Layout parser
   https://medium.com/ireadrx/table-detection-using-layout-parser-eaeb20fdba33

2. Detectron2
   https://github.com/facebookresearch/detectron2

3. Grobid
   https://python.langchain.com/docs/integrations/document_loaders/grobid/

4. Multi type TD TSR
   https://github.com/Psarpei/Multi-Type-TD-TSR

5. Layout parser
   https://layout-parser.readthedocs.io/en/latest/example/parse_ocr/

6. llamaIndex
   https://github.com/run-llama/llama_parse
   https://docs.llamaindex.ai/en/v0.10.18/examples/multi_modal/multi_modal_pdf_tables.html

7. Using Cv2
   https://medium.com/coinmonks/a-box-detection-algorithm-for-any-image-containing-boxes-756c15d7ed26

8. using hugging face 
   https://huggingface.co/foduucom/table-detection-and-extraction
   https://huggingface.co/docs/transformers/en/model_doc/table-transformer      ===> NOT Good

10. amazon-textract-textractor
   https://aws-samples.github.io/amazon-textract-textractor/notebooks/table_data_to_various_formats.html

===========> File 1.using cv2 is working corretly =============

# Using Hugging Face Model

                          +--------------------------------+
                          |  **Problem**: Table Extraction |
                          +--------------------------------+
                                          |
                                          ↓
                  +-----------------------------------------------+
                  | **Challenge**: Lack of ground truth datasets  |
                  +-----------------------------------------------+
                                          |
                                          ↓
                           +--------------------------------+
                           | **Solution**: PubTables-1M     |
                           +--------------------------------+
                                          |
            +------------------------------------------------------------+
            |  Contains:                                                 |
            |  - 1M Scientific Tables                                    |
            |  - Multi-Modal Inputs (PDFs, Images, etc.)                 |
            |  - Header & Location Info for Structure                    |
            |  - Consistency via Canonicalization (No Oversegmentation)  |
            +------------------------------------------------------------+
                                          |
                                          ↓
                     +-------------------------------------------+
                     | **Benefits**:                             |
                     | 1. Better Training Performance            |
                     | 2. Accurate Model Evaluation              |
                     | 3. Superior Model Performance             |
                     +-------------------------------------------+
                                          |
                                          ↓
               +----------------------------------------------------------+
               | **Models Trained on PubTables-1M**                       |
               | Use: Transformer-based Object Detection Models           |
               +----------------------------------------------------------+
                                          |
            +-------------------------------------+-------------------------+
            | Table Detection (Find Tables)       |                         |
            | Table Structure Recognition         |  →  Better Performance  |
            | (Rows, Columns, Headers)            |                         |
            | Functional Analysis (Role of Parts) |                         |
            +-------------------------------------+-------------------------+
