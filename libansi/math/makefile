OBJS01 = acos.obj   ceil.obj  fabs.obj   ldexp.obj  pow.obj   tan.obj    xdint.obj    xdtest.obj    xlog.obj
OBJS02 = asin.obj   cos.obj   floor.obj  log10.obj  sin.obj   tanh.obj   xdnorm.obj   xdunscal.obj  xpoly.obj
OBJS03 = atan2.obj  cosh.obj  fmod.obj   log.obj    sinh.obj  xasin.obj  xdscale.obj  xexp.obj      xsin.obj
OBJS04 = atan.obj   exp.obj   frexp.obj  modf.obj   sqrt.obj  xatan.obj  xdtento.obj  xldunsca.obj  xvalues.obj




OBJS_A = $(OBJS01) $(OBJS02) $(OBJS03) $(OBJS04)
OBJS_B = $(OBJS05) $(OBJS06) $(OBJS07) $(OBJS08)
OBJS_C = $(OBJS09) $(OBJS10) 
OBJS = $(OBJS_A) $(OBJS_B) $(OBJS_C)


LIBCNAME = ../libansi.lib
CROSSLIB = wlib
CROSSCC = wcc
#CROSSCFLAGS = -Di8088 -ms -3 -s -zls -ecc -zp1 -bt=myos -od -zq -j -zl -fo=.obj
CROSSCFLAGS = -I../_headers -Di8088 -ms -3 -s -zls -ecc -zp1 -bt=myos -od -zq -j -zl -fo=.obj -zro -fpi87 -op

all : $(LIBCNAME) 

$(LIBCNAME) : $(OBJS)
  $(CROSSLIB) -q -fo $(LIBCNAME) $(OBJS) 
 
.c.obj : 
  $(CROSSCC) $(CROSSCFLAGS) $< 
 