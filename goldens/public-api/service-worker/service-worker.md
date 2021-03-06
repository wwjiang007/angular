## API Report File for "@angular/service-worker"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { ModuleWithProviders } from '@angular/core';
import { Observable } from 'rxjs';

// @public (undocumented)
export class ServiceWorkerModule {
    static register(script: string, opts?: SwRegistrationOptions): ModuleWithProviders<ServiceWorkerModule>;
}

// @public
export class SwPush {
    constructor(sw: ɵangular_packages_service_worker_service_worker_a);
    get isEnabled(): boolean;
    readonly messages: Observable<object>;
    readonly notificationClicks: Observable<{
        action: string;
        notification: NotificationOptions & {
            title: string;
        };
    }>;
    requestSubscription(options: {
        serverPublicKey: string;
    }): Promise<PushSubscription>;
    readonly subscription: Observable<PushSubscription | null>;
    unsubscribe(): Promise<void>;
}

// @public
export abstract class SwRegistrationOptions {
    enabled?: boolean;
    registrationStrategy?: string | (() => Observable<unknown>);
    scope?: string;
}

// @public
export class SwUpdate {
    constructor(sw: ɵangular_packages_service_worker_service_worker_a);
    readonly activated: Observable<UpdateActivatedEvent>;
    // (undocumented)
    activateUpdate(): Promise<void>;
    readonly available: Observable<UpdateAvailableEvent>;
    // (undocumented)
    checkForUpdate(): Promise<void>;
    get isEnabled(): boolean;
    readonly unrecoverable: Observable<UnrecoverableStateEvent>;
}

// @public
export interface UnrecoverableStateEvent {
    // (undocumented)
    reason: string;
    // (undocumented)
    type: 'UNRECOVERABLE_STATE';
}

// @public
export interface UpdateActivatedEvent {
    // (undocumented)
    current: {
        hash: string;
        appData?: Object;
    };
    // (undocumented)
    previous?: {
        hash: string;
        appData?: Object;
    };
    // (undocumented)
    type: 'UPDATE_ACTIVATED';
}

// @public
export interface UpdateAvailableEvent {
    // (undocumented)
    available: {
        hash: string;
        appData?: Object;
    };
    // (undocumented)
    current: {
        hash: string;
        appData?: Object;
    };
    // (undocumented)
    type: 'UPDATE_AVAILABLE';
}


// (No @packageDocumentation comment for this package)

```
