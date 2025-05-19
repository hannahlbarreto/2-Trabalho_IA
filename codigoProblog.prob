% Probabilidades a priori
0.6::street(dry).
0.3::street(wet).
0.1::street(snow_covered).

0.2::flywheel_worn(t).
0.8::flywheel_worn(f).

% CPT para R (Dínamo deslizante)
0.1::r(t) :- street(dry), flywheel_worn(f).
0.5::r(t) :- street(wet); flywheel_worn(t).
0.8::r(t) :- street(snow_covered), flywheel_worn(t).
r(f) :- \+ r(t).

% CPT para V (Tensão)
0.9::voltage(t) :- r(t).
0.2::voltage(t) :- r(f).
voltage(f) :- \+ voltage(t).

% CPT para Li (Luz ligada)
0.99::light_on(t) :- voltage(t), bulb_ok(t), cable_ok(t).
0.0::light_on(t) :- \+ (voltage(t), bulb_ok(t), cable_ok(t)).

% Probabilidades a priori para B e K
0.95::bulb_ok(t).
0.9::cable_ok(t).

% Consulta para P(V|Str = snow_covered)
query(voltage(t)) :- street(snow_covered).
