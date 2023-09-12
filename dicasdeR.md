# dicas_de_R
aprendendo a trabalhar com R
library("ggplot2")
library("palmerpenguins")

ggplot(data = penguins)+
  geom_point(mapping = aes(x=flipper_length_mm,y=body_mass_g,color=species)) # cor

ggplot(data = penguins)+
  geom_point(mapping = aes(x=flipper_length_mm,y=body_mass_g,shape=species)) # figuras geometrica

ggplot(data = penguins)+
  geom_point(mapping = aes(x=flipper_length_mm,y=body_mass_g,color=species, shape=species))# cor e figures geometricas


ggplot(data = penguins)+
  geom_point(mapping = aes(x=flipper_length_mm,y=body_mass_g,color=species, shape=species, size=species))# cor, figuras geometricas e tamanhos


ggplot(data = penguins)+
  geom_point(mapping = aes(x=flipper_length_mm,y=body_mass_g),color="purple") #mudar cor

ggplot(data=penguins)+
  geom_point(mapping = aes(x=bill_length_mm,y=bill_depth_mm),color="blue")

#______________________________________________________________________________________________________________________________


ggplot(data = penguins)+
  geom_smooth(mapping = aes(x=flipper_length_mm,y=body_mass_g))+
  geom_point(mapping = aes(x=flipper_length_mm,y=body_mass_g,linetype=species))


ggplot(data = penguins)+
  geom_jitter(mapping = aes(x=flipper_length_mm,y=body_mass_g,color=species))

ggplot(data=diamonds)+
  geom_bar(mapping = aes(x=cut, fill=clarity))





###################################################################################################


ggplot(data = penguins)+
  geom_point(mapping = aes(x=flipper_length_mm,y=body_mass_g,color=species))+
  facet_wrap(~species)
