<div class="row">
    <div class="col-md-6 col-sm-8 spaced">
        <input class="form-control" placeholder="Search in Gallery" ng-model="galleryFilter" type="text"/>
    </div>
</div>

<div class="row">
    <div class="col-xs-12">
        <div class="row gallery-container">
            <div ng-repeat="article in sms.cards | filter:galleryFilter" class="col-md-4 col-sm-6">
                <div class="panel card-shadow gallery-card">
                    <a ng-href="/App/examples/{{sms.version}}/{{sms.platform}}/{{article.default || article.name}}"
                       ng-click="sms.closeSections(article.index);">
                        <div class="panel-body">
                            <div class="text-center img-wrapper">
                                <img ng-src="{{source}}/{{sms.version}}/start/{{sms.resolveImage(article)}}" />
                            </div>
                            <h3 class="text-warning">{{article.name}}</h3>
                            <p>{{article.description}}</p>
                        </div>
                    </a>
                </div>
            </div>
        </div>
    </div>
</div>
