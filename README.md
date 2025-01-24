# Algo1


VAR
    cpt_car, cpt_mot, cpt_voy: INTEGER
    ph:STRING;
    car_courant:CHAR;

BEGIN

    cpt_car:=0;
    cpt_mot:=0;
    cpt_voy:=0;
//lecture de ma phrase 
    Write("Donnez moi la phrase:")
    Read(ph);

    car_courant :=ph[0]  // exemple:car_courant:=N
    WHILE (car_courant <> '.') DO
    // je compte les caractère
        cpt_car:=cpt_car+1; 
    
        IF (car_courant = 'a' OR car_courant='A'
        OR car_courant='e' ORcar_courant='E' 
        OR car_courant='u' ORcar_courant='U'
        OR car_courant='i' OR car_courant='I'
        OR car_courant='o' OR car_courant='O' OR) THEN

             cpt_voy := cpt_voy +1;
        
        END_IF 
   
    IF (car_courant = ' ') THEN
        cpt_mot:= cpt_mot+1;
    END_IF
   car_courant:=ph[cpt_car] 
    END_WHILE
    
 cpt_car:=cpt_car+1;
 
 Write("Le nombre de caractères dans cette phrase:", cpt_car)
 Write("Le nombre de voyelles dans cette phrase:", cpt_voy)
 cpt_mot:=cpt_mot+1;
 Write("Le nombre de mots dans cette phrase:", cpt_mot)
 
END
