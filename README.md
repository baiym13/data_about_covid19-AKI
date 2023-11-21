# data_about_covid19-AKI
Import concepts about “isa”
Replace filename as your need.
LOAD CSV WITH HEADERS FROM "file:///实体.csv" AS line MERGE (c:concept{Concept:line.en,Concept_id:line.en_id, cui:line.cui, isa:line.isa, same_as:line. same_as,Usagi_en:line. Usagi_en,   Usagi_match_score:line.Usagi_match_score})
 

Import relationships about “isa”
LOAD CSV WITH HEADERS FROM "file:///三元组.csv" AS line match (from:concept{Concept_id:line.start_id}),(to:concept{Concept_id:line.end_id}) merge (from)-[r:rel{relationship:line. AFFECTS, source_sentence_count:line.source_count, Original_predicate:line. predicate_en, sentence_info:line. sentence_info, research_id:line. research_id, research_count:line.research_count, Influence_relation:line. influence_relation,Evidence_level:line.evidence_level}]->(to)

 
Import concepts and relationships about “same_as”
Replace filename as your need.
LOAD CSV WITH HEADERS FROM "file:///实体.csv" AS line MERGE (c:concept{Concept:line.en,Concept_id:line.en_id, cui:line.cui })
LOAD CSV WITH HEADERS FROM "file:///三元组.csv" AS line match (from:concept{Concept_id:line.start_id}),(to:concept{Concept_id:line.end_id}) merge (from)-[r:rel{ Original_predicate:line. predicate_en,Source:line.source, Influence_relation:line. influence_relation}]->(to)
 
Import concepts about “affectsf”
Replace filename as your need.
LOAD CSV WITH HEADERS FROM "file:///实体.csv" AS line MERGE (c:concept{Concept:line.en,Concept_id:line.en_id, cui:line.cui, isa:line.isa, same_as:line. same_as,Usagi_en:line. Usagi_en,   Usagi_match_score:line.Usagi_match_score})
 

Import relationships about “affects”
Replace filename as your need.
LOAD CSV WITH HEADERS FROM "file:///三元组.csv" AS line match (from:concept{Concept_id:line.start_id}),(to:concept{Concept_id:line.end_id}) merge (from)-[r:rel{relationship:line. AFFECTS, source_sentence_count:line.source_count, Original_predicate:line. predicate_en, sentence_info:line. sentence_info, research_id:line. research_id, research_count:line.research_count, Influence_relation:line. influence_relation,Evidence_level:line.evidence_level}]->(to)

 



