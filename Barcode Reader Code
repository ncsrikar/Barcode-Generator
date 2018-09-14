def barcode_writer(directory, location, name_column, directory_pdf):
    import pandas as pd
    import barcode
    import os 
    import img2pdf
    from PIL import Image
    from PIL import ImageFont
    from PIL import ImageDraw 
    from barcode.writer import ImageWriter                          #Diretory: Directory of the folder to save barcodes
    
    
    
    
    def fetch_data(directory,column_name,sheetname = 0):            #Location: Directory of excel file   
                                                                    #name_column: Name of the column with numbers to be barcoded
        df = pd.read_excel(directory, sheetname=0)                  #directory_pdf = directory of the of pdf file. 
        mylist = df[column_name].tolist()
        return mylist
    
    
    
    
    
  
    
    
    
    
    
    
    mylist = fetch_data( location, name_column)
    #mylist2 = fetch_data(location, "Bata")
    mylist3 = []
    mylist4 = []
    
   
    for data in mylist:
        data = str(data)
        ean = barcode.get('ean8', data, writer=ImageWriter()) 
        ean.default_writer_options['module_height'] = 3.0
        ean.default_writer_options['text_distance'] = 1.0
        directory3 = directory +"/{}"
        filename = ean.save(directory3.format(data))
        mylist3.append(filename)
    #mylist4 = list(zip(mylist3, mylist2))
    
#     for data in mylist4:
# #         print(data)
#         data_t = str(data[1])
#         filename = str(data[0])
# #         print(data_t)
        
# #         print(filename)
#         img = Image.open(filename)
#         draw = ImageDraw.Draw(img)
#         # font = ImageFont.truetype(<font-file>, <font-size>)
#         #font = ImageFont.truetype("Desktop/Aaargh.ttf", 16)
#         # draw.text((x, y),"Sample Text",(r,g,b))
#         draw.text((210,55 ),data_t,(0,0,0))
#         img.save(filename)
          
        
        
        
        
        
        
        
        
        
        
        
        
        
#     with open(directory_pdf, "ab+") as f:
#         f.write(img2pdf.convert([i for i in os.listdir(directory) if i.endswith(".png")])) 
    
