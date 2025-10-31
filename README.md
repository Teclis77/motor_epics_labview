The main vi ("motor test.vi) is located in motor_epics_labview/Software/vitruvio_4.0/membra/motor

The core vi is "motor run execution.vi" (located in the same folder) and it works with CaLab routines.

The allowed IOCs should be compiled as my other IOCs (see my other repositories); however in the global IOC vi (pectus folder), there is the list of the epics records. In the following the records list:

record,ca,prefix,label,type

stringin,$(MOT):model,VAL,status,GET 

stringin,$(MOT):err_$(card)_$(axis),VAL,error,GET 

bo,$(MOT):reqstatus_$(card)_$(axis),VAL,reqstatus,SET 

stringin,$(MOT):status_$(card)_$(axis),VAL,getstatus,GET 

bo,$(MOT):reqmotor_$(card)_$(axis),VAL,reqmotor,SET 

bo,$(MOT):reqmoving_$(card)_$(axis),VAL,reqmoving,SET 

stringin,$(MOT):moving_$(card)_$(axis),VAL,getmoving,GET 

bo,$(MOT):reqinit_$(card)_$(axis),VAL,reqinit,SET 

bo,$(MOT):reqhome_$(card)_$(axis),VAL,reqhome,SET 

bo,$(MOT):reqpos_$(card)_$(axis),VAL,reqpos,SET 

ai,$(MOT):pos_$(card)_$(axis),VAL,pos,GET 

ao,$(MOT):setma_$(card)_$(axis),VAL,moveabs,SET 

ao,$(MOT):setmr_$(card)_$(axis),VAL,moverel,SET 
