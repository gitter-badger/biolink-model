# Class: genotype to phenotypic feature association


Any association between one genotype and a phenotypic feature, where having the genotype confers the phenotype, either in isolation or through environment

URI: [http://w3id.org/biolink/vocab/GenotypeToPhenotypicFeatureAssociation](http://w3id.org/biolink/vocab/GenotypeToPhenotypicFeatureAssociation)

![img](http://yuml.me/diagram/nofunky;dir:TB/class/\[GenotypeToPhenotypicFeatureAssociation|relation:iri_type;subject_taxon_closure_label(i):label_type%20*;object_taxon_closure_label(i):label_type%20*;has_evidence(i):evidence_instance%20%3F;id(i):identifier_type%20%3F;negated(i):boolean%20%3F;association_slot(i):string%20%3F;description(i):narrative_text%20%3F]-%20object(i)>\[PhenotypicFeature],%20\[GenotypeToPhenotypicFeatureAssociation]-%20sex%20qualifier(i)%20%3F>\[BiologicalSex],%20\[GenotypeToPhenotypicFeatureAssociation]-%20onset%20qualifier(i)%20%3F>\[Onset],%20\[GenotypeToPhenotypicFeatureAssociation]-%20severity%20qualifier(i)%20%3F>\[SeverityValue],%20\[GenotypeToPhenotypicFeatureAssociation]-%20provided%20by(i)%20%3F>\[Provider],%20\[GenotypeToPhenotypicFeatureAssociation]-%20publications(i)%20*>\[Publication],%20\[GenotypeToPhenotypicFeatureAssociation]-%20qualifiers(i)%20*>\[OntologyClass],%20\[GenotypeToPhenotypicFeatureAssociation]-%20association%20type(i)%20%3F>\[OntologyClass],%20\[GenotypeToPhenotypicFeatureAssociation]-%20has%20evidence%20type(i)%20%3F>\[EvidenceType],%20\[GenotypeToPhenotypicFeatureAssociation]-%20object%20extensions(i)%20*>\[PropertyValuePair],%20\[GenotypeToPhenotypicFeatureAssociation]-%20object%20taxon%20closure(i)%20*>\[OntologyClass],%20\[GenotypeToPhenotypicFeatureAssociation]-%20object%20taxon(i)%20%3F>\[OrganismTaxon],%20\[GenotypeToPhenotypicFeatureAssociation]-%20subject%20taxon%20closure(i)%20*>\[OntologyClass],%20\[GenotypeToPhenotypicFeatureAssociation]-%20subject%20taxon(i)%20%3F>\[OrganismTaxon],%20\[GenotypeToPhenotypicFeatureAssociation]-%20subject>\[Genotype],%20\[GenotypeToPhenotypicFeatureAssociation]uses%20-.->\[EntityToPhenotypicFeatureAssociation],%20\[GenotypeToPhenotypicFeatureAssociation]uses%20-.->\[GenotypeToThingAssociation],%20\[Association]^-\[GenotypeToPhenotypicFeatureAssociation])
## Mappings

## Inheritance

 *  is_a: [Association](Association.md) - A typed association between two entities, supported by evidence
 *  mixin: [EntityToPhenotypicFeatureAssociation](EntityToPhenotypicFeatureAssociation.md)
 *  mixin: [GenotypeToThingAssociation](GenotypeToThingAssociation.md)
## Children

## Used in

## Fields

 * [genotype to phenotypic feature association.relation](genotype_to_phenotypic_feature_association_relation.md)
    * Description: the relationship type by which a subject is connected to an object in an association
    * range: [IriType](IriType.md) [required]
    * edge label: [has phenotype](has_phenotype.md) *subsets*: (translator_minimal)
    * __Local__
 * [genotype to phenotypic feature association.subject](genotype_to_phenotypic_feature_association_subject.md)
    * Description: genotype that is associated with the phenotypic feature
    * range: [Genotype](Genotype.md) [required]
    * __Local__
 * [association slot](association_slot.md)
    * Description: any slot that relates an association to another entity
    * range: **string**
    * inherited from: [Association](Association.md)
 * [association type](association_type.md)
    * Description: connects an association to the type of association (e.g. gene to phenotype)
    * range: [OntologyClass](OntologyClass.md)
    * inherited from: [Association](Association.md)
 * [association.id](association_id.md) *subsets*: (translator_minimal)
    * Description: A unique identifier for an association
    * range: [IdentifierType](IdentifierType.md)
    * inherited from: [Association](Association.md)
 * [entity to phenotypic feature association.description](entity_to_phenotypic_feature_association_description.md) *subsets*: (translator_minimal)
    * Description: A description of specific aspects of this phenotype, not otherwise covered by the phenotype ontology class
    * range: [NarrativeText](NarrativeText.md)
    * inherited from: [EntityToPhenotypicFeatureAssociation](EntityToPhenotypicFeatureAssociation.md)
 * [has evidence](has_evidence.md)
    * Description: connects an association to an instance of supporting evidence
    * range: [EvidenceInstance](EvidenceInstance.md)
    * inherited from: [ExtensionsAndEvidenceAssociationMixin](ExtensionsAndEvidenceAssociationMixin.md)
 * [has evidence type](has_evidence_type.md)
    * Description: connects an association to the class of evidence used
    * range: [EvidenceType](EvidenceType.md)
    * inherited from: [ExtensionsAndEvidenceAssociationMixin](ExtensionsAndEvidenceAssociationMixin.md)
 * [negated](negated.md)
    * Description: if set to true, then the association is negated i.e. is not true
    * range: **boolean**
    * inherited from: [Association](Association.md)
 * [object](object.md)
    * Description: connects an association to the object of the association. For example, in a gene-to-phenotype association, the gene is subject and phenotype is object.
    * range: [IriType](IriType.md) [required]
    * inherited from: [Association](Association.md)
 * [object extensions](object_extensions.md)
    * Description: Additional relationships that are true of the object in the context of the association. For example, if the object is an anatomical term in an expression association, the object extensions may include part-of links
    * range: [PropertyValuePair](PropertyValuePair.md)*
    * inherited from: [ExtensionsAndEvidenceAssociationMixin](ExtensionsAndEvidenceAssociationMixin.md)
 * [object taxon](object_taxon.md)
    * Description: the taxonomic class of the entity in the object slot
    * range: [OrganismTaxon](OrganismTaxon.md)
    * inherited from: [TaxonClosureMixin](TaxonClosureMixin.md)
 * [object taxon closure](object_taxon_closure.md)
    * Description: The taxon class or ancestor class for the object
    * range: [OntologyClass](OntologyClass.md)*
    * inherited from: [TaxonClosureMixin](TaxonClosureMixin.md)
 * [object taxon closure label](object_taxon_closure_label.md)
    * Description: The label for the taxon class or ancestor class for the object
    * range: [LabelType](LabelType.md)*
    * inherited from: [TaxonClosureMixin](TaxonClosureMixin.md)
 * [object taxon label](object_taxon_label.md)
    * range: label
    * inherited from: [TaxonClosureMixin](TaxonClosureMixin.md)
 * [onset qualifier](onset_qualifier.md)
    * Description: a qualifier used in a phenotypic association to state when the phenotype appears is in the subject
    * range: [Onset](Onset.md)
    * inherited from: [EntityToFeatureOrDiseaseQualifiers](EntityToFeatureOrDiseaseQualifiers.md)
 * [provided by](provided_by.md)
    * Description: connects an association to the agent (person, organization or group) that provided it
    * range: [Provider](Provider.md)
    * inherited from: [Association](Association.md)
 * [publications](publications.md)
    * Description: connects an association to publications supporting the association
    * range: [Publication](Publication.md)*
    * inherited from: [Association](Association.md)
 * [qualifiers](qualifiers.md)
    * Description: connects an association to qualifiers that modify or qualify the meaning of that association
    * range: [OntologyClass](OntologyClass.md)*
    * inherited from: [Association](Association.md)
 * [severity qualifier](severity_qualifier.md)
    * Description: a qualifier used in a phenotypic association to state how severe the phenotype is in the subject
    * range: [SeverityValue](SeverityValue.md)
    * inherited from: [EntityToFeatureOrDiseaseQualifiers](EntityToFeatureOrDiseaseQualifiers.md)
 * [sex qualifier](sex_qualifier.md)
    * Description: a qualifier used in a phenotypic association to state whether the association is specific to a particular sex.
    * range: [BiologicalSex](BiologicalSex.md)
    * inherited from: [EntityToPhenotypicFeatureAssociation](EntityToPhenotypicFeatureAssociation.md)
 * [subject taxon](subject_taxon.md)
    * Description: the taxonomic class of the entity in the object slot
    * range: [OrganismTaxon](OrganismTaxon.md)
    * inherited from: [TaxonClosureMixin](TaxonClosureMixin.md)
 * [subject taxon closure](subject_taxon_closure.md)
    * Description: The taxon class or ancestor class for the subject
    * range: [OntologyClass](OntologyClass.md)*
    * inherited from: [TaxonClosureMixin](TaxonClosureMixin.md)
 * [subject taxon closure label](subject_taxon_closure_label.md)
    * Description: The label for the taxon class or ancestor class for the subject
    * range: [LabelType](LabelType.md)*
    * inherited from: [TaxonClosureMixin](TaxonClosureMixin.md)
 * [subject taxon label](subject_taxon_label.md)
    * range: label
    * inherited from: [TaxonClosureMixin](TaxonClosureMixin.md)
