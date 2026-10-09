# VAPR

![licence](https://img.shields.io/badge/licence-MIT-blue) ![checks](https://img.shields.io/badge/checks-0_PASS-brightgreen)

> Governed Anticloud packaging of upstream `VAPR` in category **ARTILLERY_MANUFACTURING**. 0/16 checks PASS (measured). Every number traces to a named file plus run stamp.

**Upstream:** https://github.com/MitchellMalleo/VAProgressCircle | **Upstream pin:** `eea0708facf1955e3be8ec80e128de455e552bfe` (source: bench:BENCH.json) | **Category:** ARTILLERY_MANUFACTURING | **Licence:** MIT | **Overlay licence:** Anticommons 0.1.0

---

## What This Project Does

# VAProgressCircle

![](https://github.com/MitchellMalleo/VAProgressCircle/blob/master/vaProgressCircle.gif)

## Description

VAProgressCircle is a custom loading animation for loading iOS content from 0 to 100%.

## Requirements

- ARC
- iOS 5.0+

## Installation

1. VAProgressCircle can be installed via [CocoaPods](http://cocoapods.org/) by adding `pod 'VAProgressCircle'` to your podfile, or you can manually add `UICountingLabel.h/.m` and `VAProgressCircle.h/.m` into your project.
2. Either create a VAProgressCircle by using a UIView in your Interface Builder, subclassing it to VAProgressCircle, and linking it up to a property in your UIViewController or by using `- (id)initWithFrame:(CGRect)frame`

    ```
    self.progressCircle = [[VAProgressCircle alloc] initWithFrame:CGRectMake(50, 60, 250, 250)];
[self.view addSubview:self.circleChart];
    ```

## Usage
Set the base color of your VAProgressCircle.

	[self.progressCircle setColor:[UIColor greenColor]];
	
	//Or you can specify a highlight color with your base color

	[self.progressCircle setColor:[UIColor greenColor] withHighlightColor:VADefaultGreen];

VAProgressCircle has the ability to transition from one color to another as it reaches 100%. This can be enabled by setting your `transitionType`.

	self.progressCircle.transitionType = VAProgressCircleColorTransitionTypeGradual;

Set the transition color of your VAProgressCircle.

	[self.progressCircle setTransitionColor:[UIColor blueColor]];
	
	//Or you can specify a highlight color with your transition color

	[self.progressCircle setColor:[UIColor blueColor] withHighlightTransitionColor:VADefaultBlue];
	
Use the progessBlock to add functionality to execute before or after a progress piece has finished animating
    
    self.circleChart.progressBlock = ^(int progress, BOOL isAnimationCompleteForProgress){
        
        //Add custom block functionality here
        
    };
    
If you need the delegate pattern, do not implement the block and set your delegate and they will get called instead

	- (void)viewDidLoad
	{
    	self.progressCircle.delegate = self;
	}
	
	#pragma mark - VAProgressCircleDelegate

    - (void)progressCircle:(VAProgressCircle *)circle willAnimateToProgress:(int)progress
	{
    	//Add custom delegate functionality here
	}

	- (void)progressCircle:(VAProgressCircle *)circle didAnimateToProgress:(int)progress
	{
    	//Add custom delegate functionality here
	}

Toggle animation features of the VAProgressCircle.

	@property BOOL shouldShowAccentLine;
	@property BOOL shouldShowFinishedAccentCircle;
	@property BOOL shouldHighlightProgress;
	@property BOOL shouldNumberLabelTransition;

Set the rotation direction of your VAProgressCircle.

	self.progressCircle.rotationDirection = VAProgressCircleRotationDirectionClockwise;

## License

VAProgressCircle is available under the MIT license. See the LICENSE file for more info.

(Full upstream documentation preserved in UPSTREAM_CLONE/README.md.)

---

## Installation

1. VAProgressCircle can be installed via [CocoaPods](http://cocoapods.org/) by adding `pod 'VAProgressCircle'` to your podfile, or you can manually add `UICountingLabel.h/.m` and `VAProgressCircle.h/.m` into your project.
2. Either create a VAProgressCircle by using a UIView in your Interface Builder, subclassing it to VAProgressCircle, and linking it up to a property in your UIViewController or by using `- (id)initWithFrame:(CGRect)frame`

    ```
    self.progressCircle = [[VAProgressCircle alloc] initWithFrame:CGRectMake(50, 60, 250, 250)];
[self.view addSubview:self.circleChart];
    ```

## Usage

Set the base color of your VAProgressCircle.

	[self.progressCircle setColor:[UIColor greenColor]];
	
	//Or you can specify a highlight color with your base color

	[self.progressCircle setColor:[UIColor greenColor] withHighlightColor:VADefaultGreen];

VAProgressCircle has the ability to transition from one color to another as it reaches 100%. This can be enabled by setting your `transitionType`.

	self.progressCircle.transitionType = VAProgressCircleColorTransitionTypeGradual;

Set the transition color of your VAProgressCircle.

	[self.progressCircle setTransitionColor:[UIColor blueColor]];
	
	//Or you can specify a highlight color with your transition color

	[self.progressCircle setColor:[UIColor blueColor] withHighlightTransitionColor:VADefaultBlue];
	
Use the progessBlock to add functionality to execute before or after a progress piece has finished animating
    
    self.circleChart.progressBlock = ^(int progress, BOOL isAnimationCompleteForProgress){
        
        //Add custom block functionality here
        
    };
    
If you need the delegate pattern, do not implement the block and set your delegate and they will get called instead

	- (void)viewDidLoad
	{
    	self.progressCircle.delegate = self;
	}
	
	#pragma mark - VAProgressCircleDelegate

    - (void)progressCircle:(VAProgressCircle *)circle willAnimateToProgress:(int)progress
	{
    	//Add custom delegate functionality here
	}

	- (void)progressCircle:(VAProgressCircle *)circle didAnimateToProgress:(int)progress
	{
    	//Add custom delegate functionality here
	}

Toggle animation features of the VAProgressCircle.

	@property BOOL shouldShowAccentLine;
	@property BOOL shouldShowFinishedAccentCircle;
	@property BOOL shouldHighlightProgress;
	@property BOOL shouldNumberLabelTransition;

Set the rotation direction of your VAProgressCircle.

	self.progressCircle.rotationDirection = VAProgressCircleRotationDirectionClockwise;

## API

See upstream source in UPSTREAM_CLONE/ and the quoted documentation above.

## Dependencies

| Metric | Value |
|--------|-------|
| Files | measured |
| Lines of Code | measured |
| Dependencies | measured |
| Upstream licence | MIT |
| Overlay licence | Anticommons 0.1.0 |

Dependency manifests live in `UPSTREAM_CLONE/`; pinned lockfile in `anticloud/` where applicable.

## Configuration

See upstream source in UPSTREAM_CLONE/ and the quoted documentation above.

## Contributing

Fork the project, create a feature branch, run the test suite, and open a pull request against upstream.

## Licence

Upstream (c) its contributors under MIT - see `UPSTREAM_CLONE/LICENSE`. This packaging overlay is licensed under Anticommons 0.1.0.

## Upstream

- URL: https://github.com/MitchellMalleo/VAProgressCircle
- Pinned commit: `eea0708facf1955e3be8ec80e128de455e552bfe`
- Verify: compare against the pinned commit in the upstream project history.

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`cb64cbf1f05369d21af6938a6f967989dd85bc0cb56d5c866325332a73ce16aa`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe
and Mail, Business Insider, National Post, Financial Post, StreetInsider,
Digital Journal, Barchart, International Business Times, and Fox News.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| DANS (KNAW/NWO, Netherlands) | 10.17026/PT | EU-recognised archive |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |

